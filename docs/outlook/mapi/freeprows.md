---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438817"
---
# <a name="freeprows"></a><span data-ttu-id="e28e6-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="e28e6-103">FreeProws</span></span>

  
  
<span data-ttu-id="e28e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e28e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e28e6-105">Destrói uma estrutura [SRowSet](srowset.md) e libera memória associada, incluindo a memória alocada para todas as matrizes e estruturas membros.</span><span class="sxs-lookup"><span data-stu-id="e28e6-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e28e6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e28e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="e28e6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e28e6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e28e6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e28e6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e28e6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e28e6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e28e6-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e28e6-110">Called by:</span></span>  <br/> |<span data-ttu-id="e28e6-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="e28e6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="e28e6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e28e6-112">Parameters</span></span>

 <span data-ttu-id="e28e6-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="e28e6-113">_prows_</span></span>
  
> <span data-ttu-id="e28e6-114">[in] Ponteiro para a **estrutura SRowSet** a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="e28e6-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e28e6-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e28e6-115">Return value</span></span>

<span data-ttu-id="e28e6-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e28e6-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e28e6-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e28e6-117">Notes to callers</span></span>

<span data-ttu-id="e28e6-118">Como parte de sua implementação de **FreeProws**, o MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas na estrutura **SRowSet** antes de liberar a estrutura completa.</span><span class="sxs-lookup"><span data-stu-id="e28e6-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="e28e6-119">Portanto, todas essas entradas devem ter seguido as regras de alocação para a estrutura [SRowSet,](srowset.md) usando uma chamada [MAPIAllocateBuffer](mapiallocatebuffer.md) individual para cada matriz e estrutura de membros.</span><span class="sxs-lookup"><span data-stu-id="e28e6-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="e28e6-120">Para obter mais informações sobre como alocar memória para **estruturas ADRLIST** e **SRowSet,** consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="e28e6-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e28e6-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e28e6-121">MFCMAPI reference</span></span>

<span data-ttu-id="e28e6-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e28e6-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e28e6-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e28e6-123">**File**</span></span>|<span data-ttu-id="e28e6-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="e28e6-124">**Function**</span></span>|<span data-ttu-id="e28e6-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e28e6-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e28e6-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e28e6-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e28e6-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="e28e6-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="e28e6-128">MFCMAPI usa **o método FreeProws** para liberar uma estrutura SRowSet contendo linhas da tabela que está sendo processada.</span><span class="sxs-lookup"><span data-stu-id="e28e6-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e28e6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e28e6-129">See also</span></span>



[<span data-ttu-id="e28e6-130">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e28e6-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

