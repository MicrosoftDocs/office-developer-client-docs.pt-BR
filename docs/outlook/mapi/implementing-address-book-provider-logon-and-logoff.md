---
title: Implementando logon e logoff do provedor de agendamento de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438733"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementando logon e logoff do provedor de agendamento de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de agendamento de endereços suportam logon e logoff de sessão implementando os métodos do [IABProvider : interface IUnknown.](iabprovideriunknown.md) A interface ** IABProvider ** herda diretamente de **IUnknown** e adiciona apenas dois outros métodos: **Logon** e **Desligamento.** 
  
## <a name="logoff"></a>Logoff

O MAPI chamará o método [IABProvider::Logon](iabprovider-logon.md) do provedor no início de cada sessão e sempre que o provedor for adicionado ao perfil atual e o cliente suportar a reconfiguração dinâmica. Quando o MAPI chama o **método IABProvider::Logon,** seu provedor de agendamento inicia o processo de logon. 
  
**Para implementar IABProvider::Log**
  
1. Inicialize todos os ponteiros do parâmetro de saída passados pelo MAPI. 
    
2. Chame o método **IUnknown::AddRef** do objeto de suporte para incrementar sua contagem de referência. 
    
3. Chame o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) do objeto de suporte para abrir a seção do perfil que contém informações de configuração sobre seu provedor. Passe NULL para  _o parâmetro lpUID_ e o sinalizador MAPI_MODIFY se você pretende fazer alterações. 
    
4. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) da seção de perfil para recuperar as propriedades que seu provedor precisa para logon, como o nome do arquivo de dados ou da tabela de banco de dados. 
    
5. Verifique se as propriedades estão disponíveis e válidas. Se necessário e permitido, exiba uma caixa de diálogo para solicitar que o usuário faça correções ou adições a informações inválidas ou ausentes e chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) da seção de perfil para salvar quaisquer alterações. Algumas das propriedades comuns que devem estar disponíveis incluem: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Não defina **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). No momento do logon, essas propriedades são somente leitura. 
  
6. Se uma ou mais propriedades de configuração não estão disponíveis, falhe e retorne o valor MAPI_E_UNCONFIGURED.
    
7. Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um [MAPIUID](mapiuid.md). Seu provedor pode criar um **MAPIUID:** 
    
   - Chamando o [método IMAPISupport::NewUID.](imapisupport-newuid.md) 
    
   - Chamar a UUIDGEN.EXE para definir um GUID que seu provedor usa para incluir em um de seus arquivos de header.
    
8. Se desejado, salve um **MAPIUID** recém-criado no perfil atual chamando o método ** IMAPIProp::SetProps ** da seção de perfil. 
    
9. Libere a seção de perfil chamando seu **método IUnknown::Release.** 
    
10. In instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object. 
    
Como é possível que o MAPI chame seu método ** Logon ** várias vezes durante uma sessão, é sensato dar suporte a essa possibilidade em sua implementação, sendo capaz de criar vários objetos de logon e acompanhar cada objeto que é criado. O suporte a várias chamadas de Logon permite que um usuário de um aplicativo cliente, por exemplo, faça **logon** em uma sessão com identidades diferentes ou use destinos de entrega diferentes. 
  
**O** desligamento é chamado quando a sessão termina. O MAPI chama [o método IABProvider::Shutdown](iabprovider-shutdown.md) como uma das últimas tarefas envolvidas no desligamento de uma sessão. A MAPI liberou todos os objetos de logon do provedor e, quando o provedor recebe essa chamada, pode assumir que esta é a última chamada que receberá. Na implementação do **IABProvider::Shutdown,** execute qualquer limpeza final necessária. Por exemplo, seu provedor pode chamar **MAPIDeinitIdle** se tiver chamado **MAPIInitIdle** para usar o mecanismo ocioso durante a sessão ou o método **IUnknown::Release** de quaisquer objetos que ainda não tenham sido liberados. 
  
Se o provedor não tiver uma limpeza final, sua implementação poderá ser feita de uma única linha de código: 
  
```cpp
return S_OK;

```


