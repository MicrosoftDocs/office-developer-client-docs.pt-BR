---
title: Célula DynFeedback (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Altera o tipo de comentário visual fornecido aos usuários ao arrastar um conector. Quando o botão do mouse é liberado, a forma do conector resultante não é afetada por essa configuração não aplicável a conectores que podem ser roteados.
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771790"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="e5bc4-105">Célula DynFeedback (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="e5bc4-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="e5bc4-p102">Altera o tipo de comentário visual fornecido aos usuários ao arrastar um conector. Quando o botão do mouse é liberado, a forma do conector resultante não é afetada por essa configuração não aplicável a conectores que podem ser roteados.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="e5bc4-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-109">**Value**</span></span>|<span data-ttu-id="e5bc4-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-110">**Description**</span></span>|<span data-ttu-id="e5bc4-111">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e5bc4-112">0</span><span class="sxs-lookup"><span data-stu-id="e5bc4-112">0</span></span>  <br/> | <span data-ttu-id="e5bc4-113">Permanece reto (sem segmentos).</span><span class="sxs-lookup"><span data-stu-id="e5bc4-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="e5bc4-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="e5bc4-115">1</span><span class="sxs-lookup"><span data-stu-id="e5bc4-115">1</span></span>  <br/> | <span data-ttu-id="e5bc4-116">Mostra três segmentos quando arrastado.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="e5bc4-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="e5bc4-118">2</span><span class="sxs-lookup"><span data-stu-id="e5bc4-118">2</span></span>  <br/> | <span data-ttu-id="e5bc4-119">Mostra cinco segmentos quando arrastado.</span><span class="sxs-lookup"><span data-stu-id="e5bc4-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="e5bc4-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5bc4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5bc4-121">Remarks</span></span>

<span data-ttu-id="e5bc4-122">Para fazer referência à célula DynFeedback pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e5bc4-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5bc4-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e5bc4-123">Cell name:</span></span>  <br/> | <span data-ttu-id="e5bc4-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="e5bc4-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="e5bc4-125">Para fazer referência à célula DynFeedback pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e5bc4-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5bc4-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e5bc4-126">Section index:</span></span>  <br/> |<span data-ttu-id="e5bc4-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e5bc4-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e5bc4-128">Row index:</span></span>  <br/> |<span data-ttu-id="e5bc4-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="e5bc4-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e5bc4-130">Cell index:</span></span>  <br/> |<span data-ttu-id="e5bc4-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="e5bc4-131">**visDynFeedback**</span></span> <br/> |
   

