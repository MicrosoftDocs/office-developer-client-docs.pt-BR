---
title: Adicionar ou excluir provedores em um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 05d6d548032476062127f21b23aa2ce141ed1b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766135"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Adicionar ou excluir provedores em um serviço de mensagens

  
  
**Aplica-se a**: Outlook 
  
Para adicionar ou excluir provedores de serviços em um serviço de mensagem, use o [IProviderAdmin: IUnknown](iprovideradminiunknown.md) interface. É possível recuperar um ponteiro **IProviderAdmin** chamando [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). A tabela de provedor, está acessível por meio de [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), lista informações sobre os provedores de serviço instalado atualmente no serviço de mensagem. Clientes e provedores de serviços podem usar a tabela de provedor para acessar o nome do provedor arquivo DLL, por exemplo, ou o **MAPIUID**, o nome para exibição e o tipo de provedor, bem como informações sobre o serviço de mensagem. Para obter mais informações, consulte [As tabelas de provedor](provider-tables.md).
  
 **Para adicionar ou excluir um provedor de serviços em um serviço de mensagem**
  
1. Chame o método **AdminServices** para acessar um objeto de administração do serviço de mensagem. 
    
2. Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviços de mensagem. 
    
3. Criar uma restrição de propriedade usando uma estrutura [SPropertyRestriction](spropertyrestriction.md) que corresponda **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) com o nome do serviço de mensagem a ser modificado. 
    
4. Chame o método de [IMAPITable:: FindRow](imapitable-findrow.md) de tabela serviço de mensagens para localizar a linha do Table que representa o serviço de mensagem direcionado. 
    
5. Chame [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) para recuperar um ponteiro **IProviderAdmin** . Passe a coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha da tabela de serviço de mensagem como o parâmetro _lpUID_ . 
    
6. Chame [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) para acessar a tabela de provedor. 
    
7. Criar uma restrição de propriedade usando uma estrutura SPropertyRestriction que corresponda **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) com o nome do provedor de serviços para ser adicionado ou excluído. 
    
8. Chame o método de [IMAPITable:: FindRow](imapitable-findrow.md) da tabela provedor para localizar a linha do Table que representa o provedor de serviço de destino. 
    
9. Chame [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) para adicionar o provedor ou [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md) para removê-lo do serviço de mensagem. Para **CreateProvider**, passe a propriedade **PR_DISPLAY_NAME** do provedor como o parâmetro _lpszProvider_ . Para qualquer um dos métodos, passe a propriedade **PR_SERVICE_UID** do provedor como o parâmetro _lpUID_ . Depois que o provedor de serviço foi adicionado ou excluído, a alteração não será aparente até que uma nova sessão é criada. 
    
Outra técnica para adicionar um provedor de serviços, especificamente um provedor de armazenamento de mensagem, a um perfil envolve construindo um identificador de entrada para o provedor. Como construir um identificador de entrada requer conhecimento do seu formato, essa técnica somente poderá ser usada se o provedor de serviços tornou seu formato de identificador de entrada pública. 
  
Com o identificador de entrada construído recentemente, um cliente pode chamar [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI automaticamente cria uma seção de perfil no perfil para o provedor de serviço, mas não adicioná-lo a um serviço de mensagem. 
  
Alguns serviços de mensagem não permitir esse tipo de modificação dinâmica; ou não é suportado é até o serviço de mensagem. Outro recurso que pode ou não pode ser suportado é a capacidade de acessar diretamente seções de perfil particular do serviço de uma mensagem. Se o serviço de mensagem que você está usando permite esse tipo de acesso, ele publicará o **GUID** que representa a seção privada em MAPISVC. Você pode passar este **GUID** em uma chamada a [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) para acessar a seção de perfil. 
  

