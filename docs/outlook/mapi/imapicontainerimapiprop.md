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
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766947"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="a8a7c-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a8a7c-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="a8a7c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8a7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8a7c-105">Gerencia as operações de alto nível em objetos de contêiner como catálogos de endereços, pastas e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="a8a7c-106">O [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), e [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaces são derivados do **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8a7c-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-107">Header file:</span></span>  <br/> |<span data-ttu-id="a8a7c-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8a7c-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a8a7c-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a8a7c-110">Pasta, o contêiner de catálogo de endereços e objetos de lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="a8a7c-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="a8a7c-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8a7c-112">Armazenamento de mensagens, catálogo de endereços e provedores de transporte remoto</span><span class="sxs-lookup"><span data-stu-id="a8a7c-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="a8a7c-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-113">Called by:</span></span>  <br/> |<span data-ttu-id="a8a7c-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a8a7c-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a8a7c-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a8a7c-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a8a7c-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="a8a7c-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a8a7c-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="a8a7c-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="a8a7c-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="a8a7c-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a8a7c-120">Classe abstrata, nunca implementada</span><span class="sxs-lookup"><span data-stu-id="a8a7c-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a8a7c-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="a8a7c-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a8a7c-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="a8a7c-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="a8a7c-123">Retorna um ponteiro para a tabela de conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="a8a7c-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="a8a7c-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="a8a7c-125">Retorna um ponteiro para a tabela de hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="a8a7c-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a8a7c-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="a8a7c-127">Abre um objeto no contêiner, retornando um ponteiro de interface para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="a8a7c-128">Definir SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="a8a7c-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="a8a7c-129">Estabelece os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="a8a7c-130">Obter GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="a8a7c-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="a8a7c-131">Obtém os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="a8a7c-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="a8a7c-132">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="a8a7c-132">**Required properties**</span></span>|<span data-ttu-id="a8a7c-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="a8a7c-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8a7c-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8a7c-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a7c-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8a7c-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a7c-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8a7c-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a7c-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8a7c-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a8a7c-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a8a7c-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a8a7c-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a8a7c-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8a7c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8a7c-140">See also</span></span>



[<span data-ttu-id="a8a7c-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a8a7c-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

