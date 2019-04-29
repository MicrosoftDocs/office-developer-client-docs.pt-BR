---
title: Célula Position (Seção Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Especifica a posição de uma parada de tabulação. A posição da tabulação não depende da escala do desenho. Se o desenho estiver em escala, a posição da tabulação será a mesma.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409927"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="bc3ee-105">Célula Position (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="bc3ee-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="bc3ee-p102">Especifica a posição de uma parada de tabulação. A posição da tabulação não depende da escala do desenho. Se o desenho estiver em escala, a posição da tabulação será a mesma.</span><span class="sxs-lookup"><span data-stu-id="bc3ee-p102">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc3ee-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc3ee-109">Remarks</span></span>

<span data-ttu-id="bc3ee-110">Para fazer referência à célula Position pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="bc3ee-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc3ee-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bc3ee-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bc3ee-112">Tabula.</span><span class="sxs-lookup"><span data-stu-id="bc3ee-112">Tabs.</span></span>  <span data-ttu-id="bc3ee-113">*IJ* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bc3ee-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bc3ee-114">Para fazer referência à célula Position pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bc3ee-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc3ee-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bc3ee-115">Section index:</span></span>  <br/> |<span data-ttu-id="bc3ee-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="bc3ee-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="bc3ee-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="bc3ee-117">Row index:</span></span>  <br/> |<span data-ttu-id="bc3ee-118">**visRowTab** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc3ee-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bc3ee-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="bc3ee-119">Cell index:</span></span>  <br/> | <span data-ttu-id="bc3ee-120">(*j* \* 3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="bc3ee-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

