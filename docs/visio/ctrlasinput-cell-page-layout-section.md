---
title: Célula CtrlAsInput (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Determina a forma pai ao utilizar formas com alças de controle. Esta célula determina o comportamento de todas as formas na página de desenho.
ms.openlocfilehash: a87ba7451d73af50de4a110ecdc12b3e23e14d5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771633"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="37fef-104">Célula CtrlAsInput (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="37fef-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="37fef-p102">Determina a forma pai ao utilizar formas com alças de controle. Esta célula determina o comportamento de todas as formas na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="37fef-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="37fef-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="37fef-107">**Value**</span></span>|<span data-ttu-id="37fef-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37fef-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="37fef-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="37fef-109">TRUE</span></span>  <br/> | <span data-ttu-id="37fef-110">Define como pai a forma à qual a alça de controle está conectada.</span><span class="sxs-lookup"><span data-stu-id="37fef-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="37fef-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="37fef-111">FALSE</span></span>  <br/> | <span data-ttu-id="37fef-p103">O padrão. Define como pai a forma que contém a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="37fef-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37fef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="37fef-114">Remarks</span></span>

<span data-ttu-id="37fef-115">Para fazer referência à célula CtrlAsInput pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="37fef-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37fef-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="37fef-116">Cell name:</span></span>  <br/> | <span data-ttu-id="37fef-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="37fef-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="37fef-118">Para fazer referência à célula CtrlAsInput pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="37fef-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37fef-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="37fef-119">Section index:</span></span>  <br/> |<span data-ttu-id="37fef-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37fef-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37fef-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="37fef-121">Row index:</span></span>  <br/> |<span data-ttu-id="37fef-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="37fef-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="37fef-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="37fef-123">Cell index:</span></span>  <br/> |<span data-ttu-id="37fef-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="37fef-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

