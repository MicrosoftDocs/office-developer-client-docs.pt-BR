---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348955"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="9a6c6-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9a6c6-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="9a6c6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a6c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a6c6-105">Fornece acesso a contêineres do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-105">Provides access to address book containers.</span></span> <span data-ttu-id="9a6c6-106">MapI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a6c6-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-107">Header file:</span></span>  <br/> |<span data-ttu-id="9a6c6-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a6c6-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9a6c6-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="9a6c6-110">Objetos de contêiner do livro de endereços</span><span class="sxs-lookup"><span data-stu-id="9a6c6-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="9a6c6-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a6c6-112">Provedores de lista de endereços</span><span class="sxs-lookup"><span data-stu-id="9a6c6-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="9a6c6-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-113">Called by:</span></span>  <br/> |<span data-ttu-id="9a6c6-114">MAPI e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="9a6c6-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="9a6c6-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9a6c6-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="9a6c6-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="9a6c6-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="9a6c6-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="9a6c6-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="9a6c6-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="9a6c6-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="9a6c6-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="9a6c6-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9a6c6-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="9a6c6-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9a6c6-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="9a6c6-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="9a6c6-123">Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="9a6c6-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="9a6c6-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="9a6c6-125">Copia uma ou mais entradas, normalmente usuários de mensagens ou listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="9a6c6-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="9a6c6-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="9a6c6-127">Remove uma ou mais entradas, normalmente usuários de mensagens, listas de distribuição ou outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="9a6c6-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="9a6c6-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="9a6c6-129">Executa a resolução de nome para uma ou mais entradas de destinatário.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="9a6c6-130">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="9a6c6-130">**Required properties**</span></span>|<span data-ttu-id="9a6c6-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="9a6c6-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a6c6-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a6c6-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="9a6c6-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a6c6-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="9a6c6-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a6c6-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a6c6-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="9a6c6-142">**Propriedades opcionais**</span><span class="sxs-lookup"><span data-stu-id="9a6c6-142">**Optional properties**</span></span>|<span data-ttu-id="9a6c6-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="9a6c6-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a6c6-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a6c6-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a6c6-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-149">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a6c6-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a6c6-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a6c6-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a6c6-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a6c6-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a6c6-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a6c6-154">Remarks</span></span>

<span data-ttu-id="9a6c6-155">A interface **IABContainer** herda indiretamente da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) por meio de [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) e [IMAPIProp : interfaces IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="9a6c6-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="9a6c6-156">Os provedores de agendas implementam a interface **IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="9a6c6-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="9a6c6-157">Qualquer número de objetos de usuário de mensagens, listas de distribuição e outros contêineres de listas de endereços pode existir em um contêiner de um livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="9a6c6-158">Como em qualquer contêiner, os clientes ou provedores de serviços podem usar um contêiner de livro de endereços para abrir uma de suas entradas ou para recuperar um índice de hierarquia ou de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="9a6c6-159">Os contêineres do livro de endereços também fornecem resolução de nomes e, dependendo do provedor, a capacidade de adicionar, remover ou modificar entradas.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="9a6c6-160">MAPI define um contêiner de agenda especial chamado de pab (lista de endereços pessoal) que contém entradas copiadas de outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="9a6c6-161">Um PAB é sempre modificável.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-161">A PAB is always modifiable.</span></span> <span data-ttu-id="9a6c6-162">Os usuários geralmente preenchem sua PAB com entradas designando os destinatários com os quais eles se comunicam com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="9a6c6-163">Um PAB também pode manter endereços one-off e novos destinatários que ainda não fazem parte de qualquer contêiner do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="9a6c6-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a6c6-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a6c6-164">See also</span></span>

- [<span data-ttu-id="9a6c6-165">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9a6c6-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

