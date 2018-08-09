---
title: Tabelas de repositórios de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768141"
---
# <a name="message-store-tables"></a>Tabelas de repositórios de mensagens

  
  
**Aplica-se a**: Outlook 
  
A tabela de repositório de mensagem contém informações sobre provedores de armazenamento de mensagem no perfil atual. Há uma tabela de repositório de mensagem para cada sessão MAPI, implementada por MAPI e usado pelos clientes. Clientes podem usar essa tabela, por exemplo, para localizar todas as instâncias de um provedor específico ou para localizar um repositório de mensagem específica. 
  
A tabela de repositório de mensagens é dinâmica. Se o usuário de um aplicativo cliente edita o perfil, propriedades para os repositórios de mensagem afetada alterando o armazenamento de mensagens padrão, por exemplo, os valores da **PR_DEFAULT_STORE** são atualizadas imediatamente. 
  
Os clientes acessar a tabela de repositório de mensagens, chamando o método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
As seguintes propriedades compõem a coluna necessária definida na tabela de repositório de mensagens:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

