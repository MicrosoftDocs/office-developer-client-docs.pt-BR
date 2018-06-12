---
title: Escolher uma versão específica de MAPI para carregar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766705"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Escolher uma versão específica de MAPI para carregar

**Aplica-se a**: Outlook 
  
Quando vincular explicitamente a implementação de MAPI, você deve selecionar cuidadosamente qual implementação para carregar. 
  
Há dois métodos para vincular explicitamente a implementação de MAPI. 
  
1. Você pode carregar a biblioteca de stub MAPI e especificar no registro de uma DLL personalizada para carregar e expedir MAPI chamadas para.
    
2. Você pode implementar o algoritmo de pesquisa do cliente MAPI para pesquisar a versão do MAPI usado pelo cliente de email padrão e carregá-la.
    
Como você pode alterar as [Configurações de registro de Stub Mapi32](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) para direcionar o seu aplicativo para usar qualquer implementação de MAPI, recomendamos que você direcione o seu aplicativo para usar uma implementação do MAPI que você testadas com. A seguir descreve os dois métodos de vínculo explicitamente. 
  
## <a name="reading-from-the-registry"></a>Leitura do registro

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>Para ler informações de implementação do MAPI do registro

1. As chaves do registro que indicam uma DLL personalizada para um cliente de email estão localizadas no `HKLM\Software\Clients\Mail` chave do cliente de email. 
    
   A tabela a seguir descreve essas chaves:
    
   |**Key**|**Descrição**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Chama a uma categoria do Windows Installer PublishComponent ID (GUID) que identifica a DLL que exporta o simple MAPI ou MAPI. Se definido, esta tecla tem precedência sobre a tecla **DLLPath** ou **DLLPathEx** .  <br/> |
   |MSIApplicationLCID  <br/> |Identificador de localidade (LCID) para o seu aplicativo. A primeira sequência de valor identifica uma chave sub-recurso de `HKLM\Software` e valores de cadeia de caracteres subsequentes identificam os valores do registro sob essa chave que contêm informações de localidade.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs para Microsoft Office. A primeira sequência de valor identifica uma chave sub-recurso de `HKLM\Software` e valores de cadeia de caracteres subsequentes identificam valores sob essa chave de registro.  <br/> |
   
   Obter as informações dessas chaves.
    
2. Passe os valores que você obteve da etapa anterior para a função [FGetComponentPath](fgetcomponentpath.md) . **FGetComponentPath** é uma função que é exportada pela biblioteca de stub MAPI Mapistub. Ele retorna o caminho da versão personalizada de MAPI. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Para carregar a implementação do MAPI marcado como padrão

1. Leitura de `HKLM\Software\Clients\Mail::(default)` valor do registro. 
    
2. Procure as informações para o cliente indicado conforme descrito anteriormente.
    
> [!NOTE]
> Observe que o cliente de email padrão não pode implementar o MAPI estendido. 
  
#### <a name="example"></a>Example

Para carregar MAPI conforme implementado pelo Outlook, procure as chaves do registro em `HKLM\Software\Clients\Mail\Microsoft Outlook` e passá-las para **FGetComponentPath**. **FGetComponentPath** retornará o caminho para a implementação do Outlook de MAPI. 
  
Se as teclas **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID** não estiver definidas, verifique o valor de registro **DLLPathEx** . Se as teclas estiverem definidas, **FGetComponentPath** oferece o caminho da implementação do cliente de MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementando o algoritmo de pesquisa de cliente MAPI

A tabela a seguir lista as quatro funções de MFCMAPI que são usadas para procurar o caminho para uma implementação personalizada de MAPI:
  
|**Função**|**Descrição**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Obtém o caminho da biblioteca MAPI.  <br/> |
| `GetMailKey` <br/> |Obtém a chave de registro de email MAPI.  <br/> |
| `GetMapiMsiIds` <br/> |Obtém o identificador do Windows Installer.  <br/> |
| `GetComponentPath` <br/> |Obtém o caminho de componente usando [FGetComponentPath](fgetcomponentpath.md).  <br/> |
   
Porque MFCMAPI carrega a implementação de padrão de MAPI por padrão, se você quiser usar uma implementação diferente de MAPI, você deve explicitamente direcionar para fazê-lo. Isso é feito usando-se a rotina **Session\Load MAPI** . 
  
### <a name="how-these-functions-work"></a>Como essas funções funcionam

1. MFCMAPI chamadas `GetMAPIPath`, passar nulo para o parâmetro do cliente, a implementação de MAPI padrão de carga.
    
2.  `GetMAPIPath`chamadas `GetMapiMsiIds` ler os valores para **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`chamadas `GetMailKey` para abrir a chave do registro para o cliente de email padrão. 
    
4.  `GetMapiMsiIds`usa o identificador do registro retornado por `GetMailKey` pesquise valores para **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**.
    
5. Os valores para **MSIComponentID**, **MSIApplicationLCID**e **MSIOfficeLCID**, são retornados para `GetMAPIPath`.  `GetMAPIPath`em seguida, passa-los para `GetComponentPath`.
    
6.  `GetComponentPath`carrega a biblioteca de stub MAPI, Mapi32, do diretório do sistema. 
    
7.  `GetComponentPath`em seguida, recupera o endereço da função **FGetComponentPath** do Mapi32, supondo que o Mapi32 exporta **FGetComponentPath**.
    
8. Se obter o endereço do **FGetComponentPath** do MAPI32 falhar, `GetComponentPath` recupera o endereço de Mapistub. 
    
9.  `GetComponentPath`em seguida, chama-se **FGetComponentPath**, obtendo o caminho da versão padrão do MAPI.
    
10.  `GetMAPIPath`em seguida, retorna este caminho ao chamador, que carrega MAPI e vincula explicitamente a ele, conforme descrito no [Link para funções de MAPI](how-to-link-to-mapi-functions.md).
    
> [!NOTE] 
> - Para oferecer suporte a cópias localizadas de MAPI para inglês e localidades diferentes do inglês, `GetMAPIPath` lê os valores para as subchaves **MSIApplicationLCID** e **MSIOfficeLCID** .  `GetMAPIPath`em seguida, chama-se **FGetComponentPath**, primeiro especificando **MSIApplicationLCID** como **szQualifier**e novamente, especificando **MSIOfficeLCID** como **szQualifier**. Para obter mais informações sobre as chaves do registro para clientes de email que oferecem suporte a idiomas diferentes do inglês, consulte [Configuração de backup das MSI chaves para sua DLL de MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).   
> - Se MFCMAPI não recebe um caminho para o uso de MAPI `GetMAPIPath`, ele carrega a biblioteca de stub MAPI do diretório do sistema.
> - O valor de registro **MSMapiApps** discutido no [Mapeamento explicitamente as chamadas de MAPI para DLLs MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) só se aplica quando a biblioteca MAPI Stub é usada. Aplicativos que carregar uma implementação específica de MAPI ou a implementação de padrão de carga não precisará definir a chave de registro **MSMapiApps** . 
    
## <a name="see-also"></a>Confira também

- [FGetComponentPath](fgetcomponentpath.md)
- [Vis�o geral da programa��o MAPI](mapi-programming-overview.md)
- [Link para funções MAPI](how-to-link-to-mapi-functions.md)
- [Configurações de registro de Stub Mapi32](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [Configurando as chaves MSI para sua DLL MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [Mapeando explicitamente chamadas MAPI para DLLs MAPI](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

