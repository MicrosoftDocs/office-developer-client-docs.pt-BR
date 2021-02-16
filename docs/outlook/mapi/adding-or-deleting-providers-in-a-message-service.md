---
title: Adicionando ou excluindo provedores em um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433420"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Adicionando ou excluindo provedores em um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para adicionar ou excluir provedores de serviços em um serviço de mensagens, use o [IProviderAdmin : interface IUnknown.](iprovideradminiunknown.md) Você pode recuperar um **ponteiro IProviderAdmin** chamando [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). A tabela do provedor, acessada por meio de [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), lista informações sobre os provedores de serviços atualmente instalados no serviço de mensagens. Os clientes e provedores de serviços podem usar a tabela do provedor para acessar o nome do arquivo DLL do provedor, por exemplo, ou o **MAPIUID**, o nome de exibição e o tipo do provedor, bem como informações sobre o serviço de mensagens. Para obter mais informações, consulte Provider [Tables](provider-tables.md).
  
 **Para adicionar ou excluir um provedor de serviços em um serviço de mensagens**
  
1. Chame o **método AdminServices** para acessar um objeto de administração do serviço de mensagens. 
    
2. Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviço de mensagens. 
    
3. Crie uma restrição de propriedade usando uma estrutura [SPropertyRestriction](spropertyrestriction.md) que corresponde PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) com o nome do serviço de mensagem a ser modificado. 
    
4. Chame o método [IMAPITable::FindRow](imapitable-findrow.md) da tabela de serviço de mensagens para localizar a linha na tabela que representa o serviço de mensagens direcionadas. 
    
5. Chame [IMsgServiceAdmin::AdminProviders para](imsgserviceadmin-adminproviders.md) recuperar um ponteiro **IProviderAdmin.** Passe a **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha da tabela de serviço de mensagens como _o parâmetro lpUID._ 
    
6. Chame [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) para acessar a tabela do provedor. 
    
7. Crie uma restrição de propriedade usando uma estrutura SPropertyRestriction que corresponde PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) com o nome do provedor de serviços **a** ser adicionado ou excluído. 
    
8. Chame o método [IMAPITable::FindRow](imapitable-findrow.md) da tabela do provedor para localizar a linha na tabela que representa o provedor de serviços de o alvo. 
    
9. Chame [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) para adicionar o provedor ou [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md) para removê-lo do serviço de mensagens. Para **CreateProvider**, passe a propriedade PR_DISPLAY_NAME **provedor** como o parâmetro _lpszProvider._ Para qualquer um dos métodos, passe a propriedade PR_SERVICE_UID **provedor** como o _parâmetro lpUID._ Depois que o provedor de serviços tiver sido adicionado ou excluído, a alteração não ficará aparente até que uma nova sessão seja criada. 
    
Outra técnica para adicionar um provedor de serviços, especificamente um provedor de armazenamento de mensagens, a um perfil envolve a construção de um identificador de entrada para o provedor. Como a construção de um identificador de entrada requer conhecimento de seu formato, essa técnica só poderá ser usada se o provedor de serviços tiver feito seu formato de identificador de entrada público. 
  
Com o identificador de entrada recém-construído, um cliente pode chamar [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI automatically creates a profile section in the profile for the service provider, but does not add it to a message service. 
  
Alguns serviços de mensagem não permitem esse tipo de modificação dinâmica; se é suportado ou não é de acordo com o serviço de mensagens. Outro recurso que pode ou não ter suporte é a capacidade de acessar diretamente as seções de perfil privado de um serviço de mensagens. Se o serviço de mensagens que você está usando permitir esse acesso, ele publicará o **GUID** que representa a seção privada em MAPISVC.INF. Você pode passar esse **GUID** em uma chamada para [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) para acessar a seção de perfil. 
  

