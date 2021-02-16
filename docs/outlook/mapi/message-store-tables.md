---
title: Tabelas do Armazenamento de Mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405349"
---
# <a name="message-store-tables"></a><span data-ttu-id="f106b-103">Tabelas do Armazenamento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="f106b-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="f106b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f106b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f106b-105">A tabela do armazenamento de mensagens contém informações sobre provedores de armazenamento de mensagens no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="f106b-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="f106b-106">Há uma tabela de armazenamento de mensagens para cada sessão MAPI, implementada por MAPI e usada por clientes.</span><span class="sxs-lookup"><span data-stu-id="f106b-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="f106b-107">Os clientes podem usar essa tabela, por exemplo, para localizar todas as instâncias de um provedor específico ou para localizar um armazenamento de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="f106b-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="f106b-108">A tabela do armazenamento de mensagens é dinâmica.</span><span class="sxs-lookup"><span data-stu-id="f106b-108">The message store table is dynamic.</span></span> <span data-ttu-id="f106b-109">Se o usuário de um aplicativo cliente editar o perfil, alterando o armazenamento de mensagens padrão, por exemplo, os valores das propriedades **PR_DEFAULT_STORE** para os armazenamentos de mensagens afetados serão atualizados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f106b-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="f106b-110">Os clientes acessam a tabela do armazenamento de mensagens chamando o [método IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md)</span><span class="sxs-lookup"><span data-stu-id="f106b-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="f106b-111">As propriedades a seguir compom o conjunto de colunas necessários na tabela do armazenamento de mensagens:</span><span class="sxs-lookup"><span data-stu-id="f106b-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f106b-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f106b-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f106b-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f106b-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f106b-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f106b-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f106b-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f106b-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f106b-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f106b-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f106b-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f106b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f106b-122">See also</span></span>



[<span data-ttu-id="f106b-123">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="f106b-123">MAPI Tables</span></span>](mapi-tables.md)

