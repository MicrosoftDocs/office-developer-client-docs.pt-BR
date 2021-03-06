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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430361"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Designa um serviço de mensagens para ser o fornecedor da identidade principal do perfil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens para fornecer a identidade principal, ou NULL, que indica que **SetPrimaryIdentity** deve limpar a identidade atual. 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O serviço de mensagens foi atribuído com êxito ao fornecedor da identidade principal.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** tentou designar um serviço de mensagem que tem o sinalizador SERVICE_NO_PRIMARY_IDENTITY definido em sua **propriedade PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::SetPrimaryIdentity** estabelece um serviço de mensagens como fornecedor da identidade principal do perfil. Normalmente, a identidade principal é o usuário que está conectado ao serviço de mensagens. Ele é representado por três propriedades: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Cada provedor de serviços no serviço de mensagens designado define essas três propriedades como o nome de exibição, o identificador de entrada e a chave de pesquisa do usuário de mensagens que fornece a identidade principal. Os clientes podem recuperar o identificador de entrada da identidade principal chamando o [método IMAPISession::QueryIdentity.](imapisession-queryidentity.md) 
  
A **PR_RESOURCE_FLAGS** propriedade é definida como STATUS_PRIMARY_IDENTITY para todos os provedores que são membros do serviço de mensagens que fornece a identidade principal e SERVICE_PRIMARY_IDENTITY para o serviço de mensagens. Quando um provedor de serviços não pode fornecer a identidade principal para seu serviço de mensagens, ele **define** PR_RESOURCE_FLAGS como STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** define  PR_RESOURCE_FLAGS propriedade de cada serviço de mensagens que não está fornecendo a identidade principal para SERVICE_NO_PRIMARY_IDENTITY. 
  
Cada provedor de serviços de mensagens sobre o quais o MAPI tem informações pode estabelecer uma identidade para cada um de seus usuários quando um cliente faz o login no serviço. No entanto, como o MAPI dá suporte a conexões com vários provedores de serviços para cada sessão MAPI, não há uma definição forte da identidade de um usuário específico para a sessão MAPI como um todo; a identidade de um usuário depende de qual serviço está envolvido. Os clientes podem **chamar SetPrimaryIdentity** para designar uma das muitas identidades estabelecidas para um usuário pelos serviços de mensagem como a identidade principal desse usuário. 
  
## <a name="see-also"></a>Confira também



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

