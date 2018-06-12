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
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773042"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="ab7b3-103">Célula SpBefore (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="ab7b3-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="ab7b3-104">Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.</span><span class="sxs-lookup"><span data-stu-id="ab7b3-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab7b3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab7b3-105">Remarks</span></span>

<span data-ttu-id="ab7b3-p101">Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço anterior será a mesma.</span><span class="sxs-lookup"><span data-stu-id="ab7b3-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="ab7b3-108">Para obter uma referência à célula SpBefore pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="ab7b3-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ab7b3-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ab7b3-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ab7b3-110">Para.SpBefore [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ab7b3-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ab7b3-111">Para obter uma referência à célula SpBefore pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ab7b3-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ab7b3-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ab7b3-112">Section index:</span></span>  <br/> |<span data-ttu-id="ab7b3-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ab7b3-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="ab7b3-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ab7b3-114">Row index:</span></span>  <br/> |<span data-ttu-id="ab7b3-115">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ab7b3-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ab7b3-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ab7b3-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ab7b3-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="ab7b3-117">**visSpaceBefore**</span></span> <br/> |
   

