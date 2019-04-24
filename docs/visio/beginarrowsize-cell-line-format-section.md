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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346225"
---
# <a name="beginarrowsize-cell-line-format-section"></a><span data-ttu-id="383ac-103">Célula BeginArrowSize (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="383ac-103">BeginArrowSize Cell (Line Format Section)</span></span>

<span data-ttu-id="383ac-104">Determina o tamanho da ponta de seta no início da linha.</span><span class="sxs-lookup"><span data-stu-id="383ac-104">Determines the size of the arrowhead at the beginning of the line.</span></span>
  
|<span data-ttu-id="383ac-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="383ac-105">**Value**</span></span>|<span data-ttu-id="383ac-106">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="383ac-106">**Size**</span></span>|<span data-ttu-id="383ac-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="383ac-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="383ac-108">,0</span><span class="sxs-lookup"><span data-stu-id="383ac-108">0</span></span>  <br/> | <span data-ttu-id="383ac-109">Muito pequeno</span><span class="sxs-lookup"><span data-stu-id="383ac-109">Very small</span></span>  <br/> |<span data-ttu-id="383ac-110">**visArrowSizeVerySmall**</span><span class="sxs-lookup"><span data-stu-id="383ac-110">**visArrowSizeVerySmall**</span></span> <br/> |
| <span data-ttu-id="383ac-111">1</span><span class="sxs-lookup"><span data-stu-id="383ac-111">1</span></span>  <br/> | <span data-ttu-id="383ac-112">Small</span><span class="sxs-lookup"><span data-stu-id="383ac-112">Small</span></span>  <br/> |<span data-ttu-id="383ac-113">**visArrowSizeSmall**</span><span class="sxs-lookup"><span data-stu-id="383ac-113">**visArrowSizeSmall**</span></span> <br/> |
| <span data-ttu-id="383ac-114">duas</span><span class="sxs-lookup"><span data-stu-id="383ac-114">2</span></span>  <br/> | <span data-ttu-id="383ac-115">Média</span><span class="sxs-lookup"><span data-stu-id="383ac-115">Medium</span></span>  <br/> |<span data-ttu-id="383ac-116">**visArrowSizeMedium**</span><span class="sxs-lookup"><span data-stu-id="383ac-116">**visArrowSizeMedium**</span></span> <br/> |
| <span data-ttu-id="383ac-117">3D</span><span class="sxs-lookup"><span data-stu-id="383ac-117">3</span></span>  <br/> | <span data-ttu-id="383ac-118">Large</span><span class="sxs-lookup"><span data-stu-id="383ac-118">Large</span></span>  <br/> |<span data-ttu-id="383ac-119">**visArrowSizeLarge**</span><span class="sxs-lookup"><span data-stu-id="383ac-119">**visArrowSizeLarge**</span></span> <br/> |
| <span data-ttu-id="383ac-120">quatro</span><span class="sxs-lookup"><span data-stu-id="383ac-120">4</span></span>  <br/> | <span data-ttu-id="383ac-121">Muito grande</span><span class="sxs-lookup"><span data-stu-id="383ac-121">Very large</span></span>  <br/> |<span data-ttu-id="383ac-122">**visArrowSizeVeryLarge**</span><span class="sxs-lookup"><span data-stu-id="383ac-122">**visArrowSizeVeryLarge**</span></span> <br/> |
| <span data-ttu-id="383ac-123">0,5</span><span class="sxs-lookup"><span data-stu-id="383ac-123">5</span></span>  <br/> | <span data-ttu-id="383ac-124">Empréstimo</span><span class="sxs-lookup"><span data-stu-id="383ac-124">Jumbo</span></span>  <br/> |<span data-ttu-id="383ac-125">**visArrowSizeJumbo**</span><span class="sxs-lookup"><span data-stu-id="383ac-125">**visArrowSizeJumbo**</span></span> <br/> |
| <span data-ttu-id="383ac-126">6</span><span class="sxs-lookup"><span data-stu-id="383ac-126">6</span></span>  <br/> | <span data-ttu-id="383ac-127">Colossal</span><span class="sxs-lookup"><span data-stu-id="383ac-127">Colossal</span></span>  <br/> |<span data-ttu-id="383ac-128">**visArrowSizeColossal**</span><span class="sxs-lookup"><span data-stu-id="383ac-128">**visArrowSizeColossal**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="383ac-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="383ac-129">Remarks</span></span>

<span data-ttu-id="383ac-130">É possível também definir o tamanho da ponta de seta na caixa de diálogo **Linha**.</span><span class="sxs-lookup"><span data-stu-id="383ac-130">You can also set the size of the arrowhead in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="383ac-131">Para fazer referência à célula BeginArrowSize pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="383ac-131">To get a reference to the BeginArrowSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="383ac-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="383ac-132">Cell name:</span></span>  <br/> | <span data-ttu-id="383ac-133">BeginArrowSize</span><span class="sxs-lookup"><span data-stu-id="383ac-133">BeginArrowSize</span></span>  <br/> |
   
<span data-ttu-id="383ac-134">Para fazer referência à célula BeginArrowSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="383ac-134">To get a reference to the BeginArrowSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="383ac-135">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="383ac-135">Section index:</span></span>  <br/> |<span data-ttu-id="383ac-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="383ac-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="383ac-137">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="383ac-137">Row index:</span></span>  <br/> |<span data-ttu-id="383ac-138">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="383ac-138">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="383ac-139">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="383ac-139">Cell index:</span></span>  <br/> |<span data-ttu-id="383ac-140">**visLineBeginArrowSize**</span><span class="sxs-lookup"><span data-stu-id="383ac-140">**visLineBeginArrowSize**</span></span> <br/> |
   

