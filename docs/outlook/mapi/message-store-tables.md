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
# <a name="message-store-tables"></a><span data-ttu-id="85d85-103">Tabelas de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="85d85-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="85d85-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85d85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85d85-105">A tabela de repositório de mensagem contém informações sobre provedores de armazenamento de mensagem no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="85d85-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="85d85-106">Há uma tabela de repositório de mensagem para cada sessão MAPI, implementada por MAPI e usado pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="85d85-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="85d85-107">Clientes podem usar essa tabela, por exemplo, para localizar todas as instâncias de um provedor específico ou para localizar um repositório de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="85d85-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="85d85-108">A tabela de repositório de mensagens é dinâmica.</span><span class="sxs-lookup"><span data-stu-id="85d85-108">The message store table is dynamic.</span></span> <span data-ttu-id="85d85-109">Se o usuário de um aplicativo cliente edita o perfil, propriedades para os repositórios de mensagem afetada alterando o armazenamento de mensagens padrão, por exemplo, os valores da **PR_DEFAULT_STORE** são atualizadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="85d85-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="85d85-110">Os clientes acessar a tabela de repositório de mensagens, chamando o método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="85d85-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="85d85-111">As seguintes propriedades compõem a coluna necessária definida na tabela de repositório de mensagens:</span><span class="sxs-lookup"><span data-stu-id="85d85-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85d85-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85d85-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="85d85-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85d85-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="85d85-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85d85-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="85d85-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85d85-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="85d85-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85d85-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85d85-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85d85-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="85d85-122">See also</span></span>



[<span data-ttu-id="85d85-123">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="85d85-123">MAPI Tables</span></span>](mapi-tables.md)

