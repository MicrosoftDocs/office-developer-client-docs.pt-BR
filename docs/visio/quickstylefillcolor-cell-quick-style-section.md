---
title: Célula QuickStyleFillColor (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Determina qual cor do tema que usa o preenchimento de uma forma, como um inteiro de 0 a 7
ms.openlocfilehash: dcbb974947821327e7cff6634fd9435f5e5845bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772630"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a><span data-ttu-id="07061-103">Célula QuickStyleFillColor (Seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="07061-103">QuickStyleFillColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="07061-104">Determina qual cor do tema que usa o preenchimento de uma forma, como um inteiro de 0 a 7</span><span class="sxs-lookup"><span data-stu-id="07061-104">Determines which theme color that a shape's fill uses, as an integer from 0 to 7</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07061-105">Value</span><span class="sxs-lookup"><span data-stu-id="07061-105">Value</span></span>  <br/> |<span data-ttu-id="07061-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="07061-106">Description</span></span>  <br/> |
|<span data-ttu-id="07061-107">0</span><span class="sxs-lookup"><span data-stu-id="07061-107">0</span></span>  <br/> |<span data-ttu-id="07061-108">Herda a cor do tema escuro a cor de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="07061-108">The shape fill color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="07061-109">1</span><span class="sxs-lookup"><span data-stu-id="07061-109">1</span></span>  <br/> |<span data-ttu-id="07061-110">A cor de preenchimento da forma herda a cor do tema claro.</span><span class="sxs-lookup"><span data-stu-id="07061-110">The shape fill color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="07061-111">2</span><span class="sxs-lookup"><span data-stu-id="07061-111">2</span></span>  <br/> |<span data-ttu-id="07061-112">A cor de preenchimento da forma herda a cor do tema Ênfase 1</span><span class="sxs-lookup"><span data-stu-id="07061-112">The shape fill color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="07061-113">3</span><span class="sxs-lookup"><span data-stu-id="07061-113">3</span></span>  <br/> |<span data-ttu-id="07061-114">A cor de preenchimento da forma herda a cor do tema Ênfase 2</span><span class="sxs-lookup"><span data-stu-id="07061-114">The shape fill color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="07061-115">4</span><span class="sxs-lookup"><span data-stu-id="07061-115">4</span></span>  <br/> |<span data-ttu-id="07061-116">A cor de preenchimento da forma herda a cor do tema Ênfase 3</span><span class="sxs-lookup"><span data-stu-id="07061-116">The shape fill color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="07061-117">5</span><span class="sxs-lookup"><span data-stu-id="07061-117">5</span></span>  <br/> |<span data-ttu-id="07061-118">A cor de preenchimento da forma herda a cor do tema Ênfase 4</span><span class="sxs-lookup"><span data-stu-id="07061-118">The shape fill color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="07061-119">6</span><span class="sxs-lookup"><span data-stu-id="07061-119">6</span></span>  <br/> |<span data-ttu-id="07061-120">A cor de preenchimento da forma herda a cor do tema Ênfase 5</span><span class="sxs-lookup"><span data-stu-id="07061-120">The shape fill color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="07061-121">7</span><span class="sxs-lookup"><span data-stu-id="07061-121">7</span></span>  <br/> |<span data-ttu-id="07061-122">A cor de preenchimento da forma herda a cor do tema Ênfase 6</span><span class="sxs-lookup"><span data-stu-id="07061-122">The shape fill color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07061-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="07061-123">Remarks</span></span>

<span data-ttu-id="07061-124">Para fazer referência à célula **QuickStyleFillColor** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="07061-124">To get a reference to the **QuickStyleFillColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="07061-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="07061-125">Cell name:</span></span>  <br/> | <span data-ttu-id="07061-126">QuickStyleFillColor</span><span class="sxs-lookup"><span data-stu-id="07061-126">QuickStyleFillColor</span></span>  <br/> |
   
<span data-ttu-id="07061-127">Para obter uma referência à célula **QuickStyleFillColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="07061-127">To get a reference to the **QuickStyleFillColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="07061-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="07061-128">Section index:</span></span>  <br/> |<span data-ttu-id="07061-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="07061-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="07061-130">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="07061-130">Row index:</span></span>  <br/> |<span data-ttu-id="07061-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="07061-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="07061-132">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="07061-132">Cell index:</span></span>  <br/> |<span data-ttu-id="07061-133">**visQuickStyleFillColor**</span><span class="sxs-lookup"><span data-stu-id="07061-133">**visQuickStyleFillColor**</span></span> <br/> |
   

