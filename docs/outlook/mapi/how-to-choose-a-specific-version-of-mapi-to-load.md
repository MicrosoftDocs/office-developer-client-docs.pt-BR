---
title: Escolher uma versão MAPI específica para carregar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344517"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Escolher uma versão MAPI específica para carregar

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao vincular explicitamente a uma implementação de MAPI, você deve selecionar cuidadosamente qual implementação carregar. 
  
Há dois métodos para vincular explicitamente a uma implementação de MAPI. 
  
1. Você pode carregar a biblioteca de stub MAPI e especificar no Registro uma DLL personalizada para carregar e expedir chamadas MAPI.
    
2. Você pode implementar o algoritmo de busca do cliente MAPI para procurar a versão do MAPI usada pelo cliente de email padrão e carregá-la.
    
Como você pode alterar as configurações do RegistroMapi32.dll [ Stub](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) para direcionar seu aplicativo a usar qualquer implementação de MAPI, recomendamos direcionar seu aplicativo para usar uma implementação de MAPI testada. O exemplo a seguir descreve os dois métodos de vinculação explicitamente. 
  
## <a name="reading-from-the-registry"></a>Lendo a partir do Registro

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Para ler as informações de implementação de MAPI do Registro

1. As chaves do Registro que indicam uma DLL personalizada para um cliente de email estão localizadas na  `HKLM\Software\Clients\Mail` chave do cliente de email. 
    
   A tabela a seguir descreve estas chaves:
    
   |**Chave**|**Descrição**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Uma ID da categoria PublishComponent (GUID) do Windows Installer que identifica a DLL que exporta chamadas MAPI ou MAPI simples. Se definida, essa chave tem precedência sobre a **chave DLLPath** ou **DLLPathEx.**  <br/> |
   |MSIApplicationLCID  <br/> |Identificador de localidade (LCID) para seu aplicativo. O primeiro valor de cadeia de caracteres identifica uma sub-chave de valores subsequentes de cadeia de caracteres que identificam valores de registro sob essa chave que  `HKLM\Software` contêm informações de localidade.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs para Microsoft Office. O primeiro valor de cadeia de caracteres identifica uma sub-chave de valores subsequentes de cadeia de caracteres que identificam valores  `HKLM\Software` do Registro sob essa chave.  <br/> |
   
   Obtenha as informações dessas chaves.
    
2. Passe os valores obtidos da etapa anterior para a [função FGetComponentPath.](fgetcomponentpath.md) **FGetComponentPath** é uma função exportada pela biblioteca stub MAPI Mapistub.dll. Ele retorna o caminho da versão personalizada de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Para carregar a implementação de MAPI marcada como padrão

1. Leia o  `HKLM\Software\Clients\Mail::(default)` valor do Registro. 
    
2. Procure as informações do cliente indicado conforme descrito anteriormente.
    
> [!NOTE]
> Observe que o cliente de email padrão pode não implementar MAPI estendido. 
  
#### <a name="example"></a>Exemplo

Para carregar o MAPI conforme implementado pelo Outlook, procure as chaves do Registro e  `HKLM\Software\Clients\Mail\Microsoft Outlook` passe-as para **FGetComponentPath**. **FGetComponentPath** retornará o caminho para a implementação de MAPI do Outlook. 
  
Se as chaves **MSIComponentID**, **MSIApplicationLCID** e **MSIOfficeLCID** não estão definidas, verifique o valor do Registro **DLLPathEx.** Se as chaves estão definidas, **FGetComponentPath** fornece o caminho da implementação de MAPI do cliente. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementando o algoritmo de Busca de Cliente MAPI

A tabela a seguir lista as quatro funções de MFCMAPI que são usadas para procurar o caminho para uma implementação personalizada de MAPI:
  
|**Function**|**Description**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtém o caminho da biblioteca MAPI.  <br/> |
| `GetMailKey` <br/> |Obtém a chave do Registro de email MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtém o identificador do Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtém o caminho do componente [usando FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Como O MFCMAPI carrega a implementação padrão de MAPI por padrão, se você quiser usar uma implementação diferente do MAPI, deverá direcionar explicitamente para isso. Isso é realizado usando a rotina **Session\Load MAPI.** 
  
### <a name="how-these-functions-work"></a>Como essas funções funcionam

1. Chamadas MFCMAPI  `GetMAPIPath` , passando NULL para o parâmetro cliente, para carregar a implementação de MAPI padrão.
    
2.  `GetMAPIPath` chamadas  `GetMapiMsiIds` para ler os valores para **MSIComponentID**, **MSIApplicationLCID** e **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds` para  `GetMailKey` abrir a chave do Registro para o cliente de email padrão. 
    
4.  `GetMapiMsiIds` usa o alça do Registro retornado por para procurar valores para  `GetMailKey` **MSIComponentID**, **MSIApplicationLCID** e **MSIOfficeLCID**.
    
5. Os valores para **MSIComponentID**, **MSIApplicationLCID** e **MSIOfficeLCID**, são retornados para  `GetMAPIPath` .  `GetMAPIPath` em seguida, os passa para  `GetComponentPath` .
    
6.  `GetComponentPath` carrega a biblioteca stub MAPI, Mapi32.dll, do diretório do sistema. 
    
7.  `GetComponentPath` em seguida, recupera o endereço da **função FGetComponentPath** Mapi32.dll, supondo que Mapi32.dll **exporta FGetComponentPath**.
    
8. Se o endereço de **FGetComponentPath** Mapi32.dll falhar, recupera o  `GetComponentPath` endereço do Mapistub.dll. 
    
9.  `GetComponentPath` em **seguida, chama FGetComponentPath**, obtendo o caminho da versão padrão de MAPI.
    
10.  `GetMAPIPath` em seguida, retorna esse caminho para o chamador, que carrega MAPI e explicitamente vincula a ele conforme descrito em Link para funções [MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Para dar suporte a cópias localizadas de MAPI para localidades em inglês e não inglês, lê os valores para as `GetMAPIPath` sub-chaves **MSIApplicationLCID** e **MSIOfficeLCID.**  `GetMAPIPath` em seguida, chama **FGetComponentPath**, primeiro especificando **MSIApplicationLCID** como **szQualifier** e especificando novamente **MSIOfficeLCID** como **szQualifier**. Para obter mais informações sobre chaves do Registro para clientes de email que suportam idiomas diferentes do inglês, consulte Configurando as chaves MSI para sua [DLL MAPI.](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)   
> - Se MFCMAPI não receber um caminho para MAPI usando , ele carregará a biblioteca  `GetMAPIPath` de stub MAPI do diretório do sistema.
> - O valor do Registro **MSMapiApps** discutido no Mapeamento Explícito de Chamadas MAPI para [DLLs MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) só se aplica quando a biblioteca stub MAPI é usada. Os aplicativos que carregam uma implementação específica de MAPI ou carregam a implementação padrão não têm que definir a chave do Registro **MSMapiApps.** 
    
## <a name="see-also"></a>Confira também

- [FGetComponentPath](fgetcomponentpath.md)
- [Visão geral da programação MAPI](mapi-programming-overview.md)
- [Link para funções MAPI](how-to-link-to-mapi-functions.md)
- [Mapi32.dll do Registro stub](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Configurando as chaves MSI para sua DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Mapear explicitamente chamadas MAPI para DLLs MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

