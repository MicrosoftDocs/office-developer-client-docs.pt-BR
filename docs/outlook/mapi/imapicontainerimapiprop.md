---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406119"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="137ab-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="137ab-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="137ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="137ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="137ab-105">Gerencia operações de alto nível em objetos de contêiner, como address books, listas de distribuição e pastas.</span><span class="sxs-lookup"><span data-stu-id="137ab-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="137ab-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="137ab-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="137ab-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="137ab-107">Header file:</span></span>  <br/> |<span data-ttu-id="137ab-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="137ab-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="137ab-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="137ab-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="137ab-110">Objetos folder, address book container e distribution list</span><span class="sxs-lookup"><span data-stu-id="137ab-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="137ab-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="137ab-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="137ab-112">Armazenamento de mensagens, livro de endereços e provedores de transporte remoto</span><span class="sxs-lookup"><span data-stu-id="137ab-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="137ab-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="137ab-113">Called by:</span></span>  <br/> |<span data-ttu-id="137ab-114">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="137ab-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="137ab-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="137ab-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="137ab-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="137ab-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="137ab-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="137ab-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="137ab-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="137ab-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="137ab-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="137ab-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="137ab-120">Classe abstrata, nunca implementada</span><span class="sxs-lookup"><span data-stu-id="137ab-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="137ab-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="137ab-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="137ab-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="137ab-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="137ab-123">Retorna um ponteiro para a tabela de conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="137ab-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="137ab-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="137ab-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="137ab-125">Retorna um ponteiro para a tabela de hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="137ab-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="137ab-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="137ab-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="137ab-127">Abre um objeto no contêiner, retornando um ponteiro de interface para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="137ab-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="137ab-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="137ab-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="137ab-129">Estabelece critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="137ab-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="137ab-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="137ab-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="137ab-131">Obtém os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="137ab-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="137ab-132">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="137ab-132">**Required properties**</span></span>|<span data-ttu-id="137ab-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="137ab-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="137ab-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="137ab-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="137ab-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="137ab-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="137ab-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="137ab-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="137ab-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="137ab-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="137ab-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="137ab-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="137ab-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="137ab-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="137ab-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="137ab-140">See also</span></span>



[<span data-ttu-id="137ab-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="137ab-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

