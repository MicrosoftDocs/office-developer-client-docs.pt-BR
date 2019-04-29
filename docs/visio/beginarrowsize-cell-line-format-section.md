---
title: Célula BeginArrowSize (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Determina o tamanho da ponta de seta no início da linha.
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412279"
---
# <a name="beginarrowsize-cell-line-format-section"></a><span data-ttu-id="96534-103">Célula BeginArrowSize (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="96534-103">BeginArrowSize Cell (Line Format Section)</span></span>

<span data-ttu-id="96534-104">Determina o tamanho da ponta de seta no início da linha.</span><span class="sxs-lookup"><span data-stu-id="96534-104">Determines the size of the arrowhead at the beginning of the line.</span></span>
  
|<span data-ttu-id="96534-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="96534-105">**Value**</span></span>|<span data-ttu-id="96534-106">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="96534-106">**Size**</span></span>|<span data-ttu-id="96534-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="96534-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="96534-108">,0</span><span class="sxs-lookup"><span data-stu-id="96534-108">0</span></span>  <br/> | <span data-ttu-id="96534-109">Muito pequeno</span><span class="sxs-lookup"><span data-stu-id="96534-109">Very small</span></span>  <br/> |<span data-ttu-id="96534-110">**visArrowSizeVerySmall**</span><span class="sxs-lookup"><span data-stu-id="96534-110">**visArrowSizeVerySmall**</span></span> <br/> |
| <span data-ttu-id="96534-111">1</span><span class="sxs-lookup"><span data-stu-id="96534-111">1</span></span>  <br/> | <span data-ttu-id="96534-112">Pequeno</span><span class="sxs-lookup"><span data-stu-id="96534-112">Small</span></span>  <br/> |<span data-ttu-id="96534-113">**visArrowSizeSmall**</span><span class="sxs-lookup"><span data-stu-id="96534-113">**visArrowSizeSmall**</span></span> <br/> |
| <span data-ttu-id="96534-114">duas</span><span class="sxs-lookup"><span data-stu-id="96534-114">2</span></span>  <br/> | <span data-ttu-id="96534-115">Média</span><span class="sxs-lookup"><span data-stu-id="96534-115">Medium</span></span>  <br/> |<span data-ttu-id="96534-116">**visArrowSizeMedium**</span><span class="sxs-lookup"><span data-stu-id="96534-116">**visArrowSizeMedium**</span></span> <br/> |
| <span data-ttu-id="96534-117">3D</span><span class="sxs-lookup"><span data-stu-id="96534-117">3</span></span>  <br/> | <span data-ttu-id="96534-118">Grande</span><span class="sxs-lookup"><span data-stu-id="96534-118">Large</span></span>  <br/> |<span data-ttu-id="96534-119">**visArrowSizeLarge**</span><span class="sxs-lookup"><span data-stu-id="96534-119">**visArrowSizeLarge**</span></span> <br/> |
| <span data-ttu-id="96534-120">4 </span><span class="sxs-lookup"><span data-stu-id="96534-120">4</span></span>  <br/> | <span data-ttu-id="96534-121">Muito grande</span><span class="sxs-lookup"><span data-stu-id="96534-121">Very large</span></span>  <br/> |<span data-ttu-id="96534-122">**visArrowSizeVeryLarge**</span><span class="sxs-lookup"><span data-stu-id="96534-122">**visArrowSizeVeryLarge**</span></span> <br/> |
| <span data-ttu-id="96534-123">5 </span><span class="sxs-lookup"><span data-stu-id="96534-123">5</span></span>  <br/> | <span data-ttu-id="96534-124">Empréstimo</span><span class="sxs-lookup"><span data-stu-id="96534-124">Jumbo</span></span>  <br/> |<span data-ttu-id="96534-125">**visArrowSizeJumbo**</span><span class="sxs-lookup"><span data-stu-id="96534-125">**visArrowSizeJumbo**</span></span> <br/> |
| <span data-ttu-id="96534-126">6 </span><span class="sxs-lookup"><span data-stu-id="96534-126">6</span></span>  <br/> | <span data-ttu-id="96534-127">Colossal</span><span class="sxs-lookup"><span data-stu-id="96534-127">Colossal</span></span>  <br/> |<span data-ttu-id="96534-128">**visArrowSizeColossal**</span><span class="sxs-lookup"><span data-stu-id="96534-128">**visArrowSizeColossal**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96534-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="96534-129">Remarks</span></span>

<span data-ttu-id="96534-130">É possível também definir o tamanho da ponta de seta na caixa de diálogo **Linha**.</span><span class="sxs-lookup"><span data-stu-id="96534-130">You can also set the size of the arrowhead in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="96534-131">Para fazer referência à célula BeginArrowSize pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="96534-131">To get a reference to the BeginArrowSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96534-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="96534-132">Cell name:</span></span>  <br/> | <span data-ttu-id="96534-133">BeginArrowSize</span><span class="sxs-lookup"><span data-stu-id="96534-133">BeginArrowSize</span></span>  <br/> |
   
<span data-ttu-id="96534-134">Para fazer referência à célula BeginArrowSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="96534-134">To get a reference to the BeginArrowSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96534-135">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="96534-135">Section index:</span></span>  <br/> |<span data-ttu-id="96534-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="96534-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="96534-137">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="96534-137">Row index:</span></span>  <br/> |<span data-ttu-id="96534-138">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="96534-138">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="96534-139">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="96534-139">Cell index:</span></span>  <br/> |<span data-ttu-id="96534-140">**visLineBeginArrowSize**</span><span class="sxs-lookup"><span data-stu-id="96534-140">**visLineBeginArrowSize**</span></span> <br/> |
   

