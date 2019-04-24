---
title: Implementar o logon e logoff do provedor de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332925"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementar o logon e logoff do provedor de catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de catálogos de endereços dão suporte ao logon e ao logoff da sessão implementando os métodos da interface [IABProvider: IUnknown](iabprovideriunknown.md) . A interface * * IABProvider * * herda diretamente de **IUnknown** e adiciona apenas dois outros métodos: **logon** e **Shutdown**. 
  
## <a name="logoff"></a>Logoff

O MAPI chamará o método [IABProvider:: logon](iabprovider-logon.md) do provedor no início de cada sessão e sempre que seu provedor for adicionado ao perfil atual e o cliente oferecerá suporte à reconfiguração dinâmica. Quando MAPI chama o método **IABProvider:: logon** , seu provedor de catálogo de endereços inicia o processo de logon. 
  
**Para implementar o IABProvider:: log**
  
1. Inicializar todos os ponteiros de parâmetro de saída passados por MAPI. 
    
2. Chame o método **IUnknown:: AddRef** do objeto support para incrementar sua contagem de referência. 
    
3. Chame o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) do objeto support para abrir a seção do perfil que contém informações de configuração sobre seu provedor. Passe NULL para o parâmetro _lpUID_ e o sinalizador MAPI_MODIFY se você pretende fazer alterações. 
    
4. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps da seção de perfil para recuperar as propriedades que seu provedor precisa para o logon, como o nome do arquivo de dados ou a tabela de banco de dados. 
    
5. Verifique se as propriedades estão disponíveis e são válidas. Se necessário e permitido, exiba uma caixa de diálogo para solicitar que o usuário faça correções ou inclusões em informações inválidas ou ausentes e chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps da seção de perfil para salvar as alterações. Algumas das propriedades comuns que devem estar disponíveis incluem: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Não defina **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). No momento do logon, essas propriedades são somente leitura. 
  
6. Se uma ou mais propriedades de configuração não estiverem disponíveis, falhará e retornará o valor MAPI_E_UNCONFIGURED.
    
7. Chamar [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar um [MAPIUID](mapiuid.md). O provedor pode criar um **MAPIUID** : 
    
   - Chamar o método [IMAPISupport:: NewUID](imapisupport-newuid.md) . 
    
   - Chamar o UUIDGEN. EXE para definir um GUID que seu provedor usa para incluir em um de seus arquivos de cabeçalho.
    
8. Se quiser, salve um **MAPIUID** recém-criado no perfil atual chamando o método * * IMAPIProp:: SetProps * * da seção de perfil. 
    
9. Solte a seção Profile chamando seu método **IUnknown:: Release** . 
    
10. Crie uma instância de um novo objeto de logon e defina o conteúdo do parâmetro _lppABLogon_ para o endereço desse novo objeto. 
    
Como é possível para o MAPI chamar o método * * login * * várias vezes durante uma sessão, é prudente dar suporte a essa possibilidade na sua implementação, sendo capaz de criar vários objetos de logon e manter o controle de cada objeto criado. O suporte a várias chamadas de **logon** permite que um usuário de um aplicativo cliente, por exemplo, faça logon em uma sessão com identidades diferentes ou use diferentes destinos de entrega. 
  
**Shutdown** é chamado quando a sessão está terminando. O MAPI chama o método [IABProvider:: Shutdown](iabprovider-shutdown.md) como uma das últimas tarefas envolvidas ao desligar uma sessão. O MAPI lançou todos os objetos de logon do provedor e, quando o seu provedor receber essa chamada, poderá supor que esta é a última chamada que receberá. Em sua implementação do **IABProvider:: Shutdown**, execute qualquer limpeza final que você achar necessário. Por exemplo, seu provedor pode chamar **MAPIDeinitIdle** se tiver chamado **MAPIInitIdle** para usar o mecanismo de ociosidade durante a sessão ou o método **IUnknown:: Release** de todos os objetos que ainda devem ser liberados. 
  
Se o provedor não tiver uma limpeza final, sua implementação poderá ser composta por uma única linha de código: 
  
```cpp
return S_OK;

```


