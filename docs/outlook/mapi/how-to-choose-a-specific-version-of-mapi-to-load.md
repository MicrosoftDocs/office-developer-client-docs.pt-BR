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
  
Ao vincular explicitamente a uma implementação de MAPI, você deve selecionar cuidadosamente a implementação a ser carregada. 
  
Há dois métodos para vincular explicitamente a uma implementação de MAPI. 
  
1. Você pode carregar a biblioteca de stub MAPI e especificar no registro uma DLL personalizada para carregar e distribuir as chamadas MAPI para.
    
2. Você pode implementar o algoritmo de pesquisa de cliente MAPI para pesquisar a versão de MAPI usada pelo cliente de email padrão e carregá-lo.
    
Como você pode alterar as [configurações do registro stub de Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) para direcionar seu aplicativo para usar qualquer implementação de MAPI, recomendamos que você direcione seu aplicativo para usar uma implementação de MAPI que você testou com. O procedimento a seguir descreve os dois métodos de vinculação explícita. 
  
## <a name="reading-from-the-registry"></a>Leitura do registro

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Para ler as informações de implementação de MAPI do registro

1. As chaves do registro que indicam uma DLL personalizada para um cliente de email estão localizadas na `HKLM\Software\Clients\Mail` chave do cliente de email. 
    
   A tabela a seguir descreve estas chaves:
    
   |**Tecla**|**Descrição**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Uma ID de categoria (GUID) PublishComponent do Windows Installer que identifica a DLL que exporta as chamadas simples de MAPI ou MAPI. Se definido, esta tecla tem precedência sobre a chave **DLLPath** ou **DLLPathEx** .  <br/> |
   |MSIApplicationLCID  <br/> |Identificador de localidade (LCID) do seu aplicativo. O primeiro valor de cadeia de caracteres identifica uma subchave de e os valores de cadeia de `HKLM\Software` caracteres subsequentes identificam os valores do registro sob esta chave que contêm informações de localidade.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs do Microsoft Office. O primeiro valor de cadeia de caracteres identifica uma subchave de e os valores de cadeia de `HKLM\Software` caracteres subsequentes identificam os valores do registro sob essa chave.  <br/> |
   
   Obtenha as informações dessas chaves.
    
2. Passe os valores obtidos da etapa anterior para a função [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** é uma função que é exportada pela biblioteca de stub de MAPI MAPISTUB. dll. Ele retorna o caminho da versão personalizada de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Para carregar a implementação de MAPI marcada como padrão

1. Leia o `HKLM\Software\Clients\Mail::(default)` valor do registro. 
    
2. Procure as informações para o cliente indicado, conforme descrito anteriormente.
    
> [!NOTE]
> Observe que o cliente de email padrão pode não implementar o MAPI estendido. 
  
#### <a name="example"></a>Exemplo

Para carregar MAPI conforme implementado pelo Outlook, procure as chaves do registro em `HKLM\Software\Clients\Mail\Microsoft Outlook` e passe-as para o **FGetComponentPath**. **FGetComponentPath** retornará o caminho para a implementação de MAPI do Outlook. 
  
Se as chaves **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID** não estiverem definidas, verifique o valor do registro **DLLPathEx** . Se as chaves estiverem definidas, **FGetComponentPath** fornecerá o caminho da implementação de MAPI do cliente. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementar o algoritmo de pesquisa de cliente MAPI

A tabela a seguir lista as quatro funções do MFCMAPI que são usadas para pesquisar o caminho de uma implementação personalizada de MAPI:
  
|**Function**|**Descrição**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtém o caminho da biblioteca MAPI.  <br/> |
| `GetMailKey` <br/> |Obtém a chave de registro de email MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtém o identificador do Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtém o caminho do componente usando [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Como o MFCMAPI carrega a implementação padrão de MAPI por padrão, se você quiser usar uma implementação diferente de MAPI, é necessário direcioná-lo explicitamente para isso. Isso é feito usando a rotina **MAPI Session\Load** . 
  
### <a name="how-these-functions-work"></a>Como essas funções funcionam

1. Chamadas `GetMAPIPath`MFCMAPI, passando NULL para o parâmetro Client, para carregar a implementação MAPI padrão.
    
2.  `GetMAPIPath`chamadas `GetMapiMsiIds` para ler os valores de **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`chamadas `GetMailKey` para abrir a chave do registro para o cliente de email padrão. 
    
4.  `GetMapiMsiIds`usa o identificador do registro retornado `GetMailKey` por para pesquisar valores de **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.
    
5. Os valores de **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**são retornados para `GetMAPIPath`.  `GetMAPIPath`em seguida, passa `GetComponentPath`-os para o.
    
6.  `GetComponentPath`carrega a biblioteca de stub MAPI, Mapi32. dll, do diretório do sistema. 
    
7.  `GetComponentPath`em seguida, recupera o endereço da função **FGetComponentPath** de Mapi32. dll, supondo que Mapi32. dll exporta **FGetComponentPath**.
    
8. Se a obter o endereço de **FGetComponentPath** de Mapi32. dll falhar `GetComponentPath` , o recuperará o endereço de MAPISTUB. dll. 
    
9.  `GetComponentPath`em seguida, chama **FGetComponentPath**, obtendo o caminho da versão padrão do MAPI.
    
10.  `GetMAPIPath`em seguida, retorna esse caminho para o chamador, que carrega o MAPI e explicitamente os links para ele, conforme descrito em [link to MAPI Functions](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Para dar suporte a cópias localizadas de MAPI para localidades do inglês e `GetMAPIPath` que não sejam do inglês, lê os valores das subchaves **MSIApplicationLCID** e **MSIOfficeLCID** .  `GetMAPIPath`em seguida, chama **FGetComponentPath**, primeiro especificando **MSIApplicationLCID** como **szQualifier**e, novamente, especificando **MSIOfficeLCID** como **szQualifier**. Para obter mais informações sobre chaves do registro para clientes de email que oferecem suporte a idiomas que não são do inglês, confira conFigurando [as chaves msi para sua dll MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Se o MFCMAPI não receber um caminho para MAPI usando `GetMAPIPath`o, ele carregará a biblioteca de stub MAPI do diretório do sistema.
> - O valor do registro **MSMapiApps** discutido em [mapeamento explicitamente de chamadas MAPI para DLLs MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) só se aplica quando a biblioteca stub MAPI é usada. Os aplicativos que carregam uma implementação específica de MAPI ou carregam a implementação padrão não precisam definir a chave do registro **MSMapiApps** . 
    
## <a name="see-also"></a>Confira também

- [FGetComponentPath](fgetcomponentpath.md)
- [Visão geral da programação MAPI](mapi-programming-overview.md)
- [Link para funções MAPI](how-to-link-to-mapi-functions.md)
- [Configurações do registro stub Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [ConFigurando as chaves MSI para sua DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Mapear explicitamente as chamadas MAPI para DLLs MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

