---
title: Tabelas de repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356893"
---
# <a name="message-store-tables"></a>Tabelas de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela repositório de mensagens contém informações sobre provedores de repositórios de mensagens no perfil atual. Há uma tabela de repositório de mensagens para cada sessão MAPI, implementada por MAPI e usada por clientes. Os clientes podem usar essa tabela, por exemplo, para localizar todas as instâncias de um provedor específico ou para localizar um repositório de mensagens específico. 
  
A tabela do repositório de mensagens é dinâmica. Se o usuário de um aplicativo cliente edita o perfil, alterando o repositório de mensagens padrão, por exemplo, os valores das propriedades **PR_DEFAULT_STORE** para os repositórios de mensagens afetados são imediatamente atualizados. 
  
Os clientes acessam a tabela do repositório de mensagens chamando o método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
As propriedades a seguir compõem o conjunto de colunas necessárias na tabela do repositório de mensagens:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

