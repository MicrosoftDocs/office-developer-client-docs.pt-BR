---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767484"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Aplica-se a**: Outlook 
  
Designa um serviço de mensagem a ser o fornecedor da identidade principal para o perfil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem para fornecer a identidade principal, ou nulo, o que indica que o **SetPrimaryIdentity** deve desmarcar a identidade atual. 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O serviço de mensagem foi atribuído com êxito o fornecedor da identidade principal.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** tentou designar um serviço de mensagem que tem o sinalizador SERVICE_NO_PRIMARY_IDENTITY definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::SetPrimaryIdentity** estabelece um serviço de mensagem como o fornecedor da identidade principal para o perfil. A identidade principal é normalmente o usuário que está conectado ao serviço de mensagem. Ela é representada por três propriedades: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Cada provedor de serviço no serviço de mensagem designada define essas três propriedades como o nome para exibição, o identificador de entrada e a chave de pesquisa do usuário mensagens que fornece a identidade principal. Os clientes podem recuperar o identificador de entrada a identidade principal chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) . 
  
A propriedade **PR_RESOURCE_FLAGS** é definida para STATUS_PRIMARY_IDENTITY para cada provedor que seja membro do serviço de mensagem que fornece a identidade principal e SERVICE_PRIMARY_IDENTITY para o serviço de mensagem. Quando um provedor de serviços, será possível fornecer a identidade do principal para o seu serviço de mensagem, ela define **PR_RESOURCE_FLAGS** para STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** define a propriedade **PR_RESOURCE_FLAGS** de cada serviço de mensagem que não está fornecendo a identidade principal a SERVICE_NO_PRIMARY_IDENTITY. 
  
Cada provedor de serviços de mensagem MAPI tem informações sobre pode estabelecer uma identidade de cada um dos seus usuários quando um cliente fizer logon no serviço. No entanto, como MAPI oferece suporte a conexões com vários provedores de serviço para cada sessão MAPI, há uma estável definição da identidade de um usuário específico para a sessão MAPI como um todo; a identidade do usuário depende de qual serviço está envolvido. Os clientes podem chamar **SetPrimaryIdentity** para designar uma das muitas identidades estabelecidas para um usuário pelos serviços de mensagem como a identidade do principal para esse usuário. 
  
## <a name="see-also"></a>Confira também



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

