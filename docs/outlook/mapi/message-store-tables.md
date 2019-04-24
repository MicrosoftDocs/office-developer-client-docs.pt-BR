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
# <a name="message-store-tables"></a><span data-ttu-id="faa0e-103">Tabelas de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="faa0e-103">Message Store Tables</span></span>

  
  
<span data-ttu-id="faa0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faa0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faa0e-105">A tabela repositório de mensagens contém informações sobre provedores de repositórios de mensagens no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="faa0e-105">The message store table contains information about message store providers in the current profile.</span></span> <span data-ttu-id="faa0e-106">Há uma tabela de repositório de mensagens para cada sessão MAPI, implementada por MAPI e usada por clientes.</span><span class="sxs-lookup"><span data-stu-id="faa0e-106">There is one message store table for every MAPI session, implemented by MAPI and used by clients.</span></span> <span data-ttu-id="faa0e-107">Os clientes podem usar essa tabela, por exemplo, para localizar todas as instâncias de um provedor específico ou para localizar um repositório de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="faa0e-107">Clients can use this table, for example, to locate all instances of a particular provider or to locate a specific message store.</span></span> 
  
<span data-ttu-id="faa0e-108">A tabela do repositório de mensagens é dinâmica.</span><span class="sxs-lookup"><span data-stu-id="faa0e-108">The message store table is dynamic.</span></span> <span data-ttu-id="faa0e-109">Se o usuário de um aplicativo cliente edita o perfil, alterando o repositório de mensagens padrão, por exemplo, os valores das propriedades **PR_DEFAULT_STORE** para os repositórios de mensagens afetados são imediatamente atualizados.</span><span class="sxs-lookup"><span data-stu-id="faa0e-109">If the user of a client application edits the profile, changing the default message store, for example, the values of the **PR_DEFAULT_STORE** properties for the affected message stores are immediately updated.</span></span> 
  
<span data-ttu-id="faa0e-110">Os clientes acessam a tabela do repositório de mensagens chamando o método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) .</span><span class="sxs-lookup"><span data-stu-id="faa0e-110">Clients access the message store table by calling the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method.</span></span> 
  
<span data-ttu-id="faa0e-111">As propriedades a seguir compõem o conjunto de colunas necessárias na tabela do repositório de mensagens:</span><span class="sxs-lookup"><span data-stu-id="faa0e-111">The following properties make up the required column set in the message store table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="faa0e-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-112">**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="faa0e-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="faa0e-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-114">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="faa0e-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-115">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="faa0e-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-116">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="faa0e-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="faa0e-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-118">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="faa0e-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="faa0e-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-120">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="faa0e-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="faa0e-121">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faa0e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="faa0e-122">See also</span></span>



[<span data-ttu-id="faa0e-123">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="faa0e-123">MAPI Tables</span></span>](mapi-tables.md)

