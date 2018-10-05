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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392183"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="5ed77-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5ed77-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="5ed77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ed77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ed77-105">Fornece acesso aos contêineres do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ed77-105">Provides access to address book containers.</span></span> <span data-ttu-id="5ed77-106">Aplicativos MAPI e cliente chamam os métodos de **IABContainer** para realizar a resolução de nomes e para criar, copiar e exclua os destinatários.</span><span class="sxs-lookup"><span data-stu-id="5ed77-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ed77-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5ed77-107">Header file:</span></span>  <br/> |<span data-ttu-id="5ed77-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ed77-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5ed77-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="5ed77-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5ed77-110">Objetos de contêiner de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5ed77-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="5ed77-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5ed77-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5ed77-112">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="5ed77-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="5ed77-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5ed77-113">Called by:</span></span>  <br/> |<span data-ttu-id="5ed77-114">Aplicativos MAPI e cliente</span><span class="sxs-lookup"><span data-stu-id="5ed77-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="5ed77-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="5ed77-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5ed77-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="5ed77-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="5ed77-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="5ed77-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5ed77-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="5ed77-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="5ed77-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="5ed77-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="5ed77-120">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="5ed77-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5ed77-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="5ed77-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5ed77-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5ed77-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="5ed77-123">Cria uma nova entrada, que pode ser um usuário de mensagens, uma lista de distribuição ou outro contêiner.</span><span class="sxs-lookup"><span data-stu-id="5ed77-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="5ed77-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="5ed77-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="5ed77-125">Copia uma ou mais entradas, os usuários geralmente mensagens ou listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="5ed77-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="5ed77-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="5ed77-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="5ed77-127">Remove uma ou mais entradas, normalmente mensagens outros contêineres, listas de distribuição ou os usuários.</span><span class="sxs-lookup"><span data-stu-id="5ed77-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="5ed77-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5ed77-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="5ed77-129">Executa a resolução de nomes para uma ou mais entradas de destinatário.</span><span class="sxs-lookup"><span data-stu-id="5ed77-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="5ed77-130">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="5ed77-130">**Required properties**</span></span>|<span data-ttu-id="5ed77-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="5ed77-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ed77-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5ed77-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="5ed77-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5ed77-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="5ed77-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ed77-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ed77-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="5ed77-142">**Propriedades opcionais**</span><span class="sxs-lookup"><span data-stu-id="5ed77-142">**Optional properties**</span></span>|<span data-ttu-id="5ed77-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="5ed77-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ed77-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ed77-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ed77-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-149">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ed77-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ed77-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ed77-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ed77-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ed77-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ed77-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ed77-154">Remarks</span></span>

<span data-ttu-id="5ed77-155">A interface **IABContainer** herda indiretamente da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) por meio do [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) e [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="5ed77-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="5ed77-156">Provedores de catálogo de endereços implementam a interface de **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="5ed77-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="5ed77-157">Qualquer número de objetos de usuário de mensagens, listas de distribuição e outros contêineres do catálogo de endereços pode existir em um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ed77-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="5ed77-158">Assim como acontece com qualquer contêiner, clientes ou provedores de serviços podem usar um contêiner de catálogo de endereços para abrir uma das suas entradas ou para recuperar uma tabela de hierarquia ou a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5ed77-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="5ed77-159">Contêineres também fornecem resolução de nomes e, dependendo de provedor, a capacidade de adicionar, remover ou modificar entradas de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ed77-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="5ed77-160">MAPI define um contêiner de catálogo de endereços especial chamado o catálogo de endereços pessoal (PAB) que contém as entradas copiadas de outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="5ed77-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="5ed77-161">Um PAB sempre é modificável.</span><span class="sxs-lookup"><span data-stu-id="5ed77-161">A PAB is always modifiable.</span></span> <span data-ttu-id="5ed77-162">Os usuários preenchem geralmente seu PAB com entradas designar os destinatários com o qual se comunicam com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="5ed77-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="5ed77-163">Um PAB também pode manter endereços únicos e novos destinatários ainda não parte de qualquer contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5ed77-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5ed77-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ed77-164">See also</span></span>

- [<span data-ttu-id="5ed77-165">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5ed77-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

