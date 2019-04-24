---
title: Célula SpBefore (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329880"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="c5729-103">Célula SpBefore (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="c5729-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="c5729-104">Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.</span><span class="sxs-lookup"><span data-stu-id="c5729-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5729-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5729-105">Remarks</span></span>

<span data-ttu-id="c5729-p101">Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço anterior será a mesma.</span><span class="sxs-lookup"><span data-stu-id="c5729-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="c5729-108">Para fazer referência à célula SpBefore pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c5729-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5729-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c5729-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c5729-110">Para. antes de [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c5729-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c5729-111">Para fazer referência à célula SpBefore pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c5729-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5729-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c5729-112">Section index:</span></span>  <br/> |<span data-ttu-id="c5729-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c5729-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c5729-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c5729-114">Row index:</span></span>  <br/> |<span data-ttu-id="c5729-115">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c5729-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c5729-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c5729-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c5729-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="c5729-117">**visSpaceBefore**</span></span> <br/> |
   

