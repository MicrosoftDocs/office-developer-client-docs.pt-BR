---
title: Célula Width (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Contém a largura da forma selecionada em unidades de desenho. A fórmula padrão para determinar a largura de uma forma 1D é:'
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773278"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="289f2-104">Célula Width (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="289f2-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="289f2-p102">Contém a largura da forma selecionada em unidades de desenho. A fórmula padrão para determinar a largura de uma forma 1D é:</span><span class="sxs-lookup"><span data-stu-id="289f2-p102">Contains the width of the selected shape in drawing units. The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="289f2-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="289f2-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="289f2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="289f2-108">Remarks</span></span>

<span data-ttu-id="289f2-109">Para fazer referência à célula Width pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="289f2-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="289f2-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="289f2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="289f2-111">Width</span><span class="sxs-lookup"><span data-stu-id="289f2-111">Width</span></span>  <br/> |
   
<span data-ttu-id="289f2-112">Para fazer referência à célula Width pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="289f2-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="289f2-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="289f2-113">Section index:</span></span>  <br/> |<span data-ttu-id="289f2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="289f2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="289f2-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="289f2-115">Row index:</span></span>  <br/> |<span data-ttu-id="289f2-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="289f2-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="289f2-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="289f2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="289f2-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="289f2-118">**visXFormWidth**</span></span> <br/> |
   

