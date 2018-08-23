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
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575697"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="4092b-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4092b-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="4092b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4092b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4092b-105">Gerencia as operações de alto nível em objetos de contêiner como catálogos de endereços, pastas e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="4092b-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="4092b-106">O [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), e [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaces são derivados do **IMAPIContainer**.</span><span class="sxs-lookup"><span data-stu-id="4092b-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4092b-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4092b-107">Header file:</span></span>  <br/> |<span data-ttu-id="4092b-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4092b-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4092b-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="4092b-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="4092b-110">Pasta, o contêiner de catálogo de endereços e objetos de lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="4092b-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="4092b-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4092b-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="4092b-112">Armazenamento de mensagens, catálogo de endereços e provedores de transporte remoto</span><span class="sxs-lookup"><span data-stu-id="4092b-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="4092b-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4092b-113">Called by:</span></span>  <br/> |<span data-ttu-id="4092b-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="4092b-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="4092b-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="4092b-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4092b-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="4092b-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="4092b-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="4092b-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="4092b-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="4092b-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="4092b-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="4092b-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="4092b-120">Classe abstrata, nunca implementada</span><span class="sxs-lookup"><span data-stu-id="4092b-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4092b-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="4092b-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4092b-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="4092b-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="4092b-123">Retorna um ponteiro para a tabela de conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4092b-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="4092b-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="4092b-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="4092b-125">Retorna um ponteiro para a tabela de hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4092b-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="4092b-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4092b-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="4092b-127">Abre um objeto no contêiner, retornando um ponteiro de interface para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="4092b-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="4092b-128">Definir SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4092b-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="4092b-129">Estabelece os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="4092b-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="4092b-130">Obter GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4092b-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="4092b-131">Obtém os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="4092b-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="4092b-132">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="4092b-132">**Required properties**</span></span>|<span data-ttu-id="4092b-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="4092b-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4092b-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4092b-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4092b-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4092b-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="4092b-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4092b-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4092b-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4092b-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="4092b-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4092b-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4092b-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4092b-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4092b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="4092b-140">See also</span></span>



[<span data-ttu-id="4092b-141">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4092b-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

