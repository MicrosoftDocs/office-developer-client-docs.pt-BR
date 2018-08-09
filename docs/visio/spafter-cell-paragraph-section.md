---
title: Célula SpAfter (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Determina a quantidade de espaço inserido depois de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o último parágrafo em um bloco de texto, da célula BottomMargin.
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773065"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="99853-103">Célula SpAfter (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="99853-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="99853-104">Determina a quantidade de espaço inserido depois de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o último parágrafo em um bloco de texto, da célula BottomMargin.</span><span class="sxs-lookup"><span data-stu-id="99853-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99853-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="99853-105">Remarks</span></span>

<span data-ttu-id="99853-p101">Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço após será a mesma.</span><span class="sxs-lookup"><span data-stu-id="99853-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="99853-108">Para fazer referência à célula SpAfter pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="99853-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99853-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="99853-109">Cell name:</span></span>  <br/> | <span data-ttu-id="99853-110">Para.SpAfter [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="99853-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="99853-111">Para fazer referência à célula SpAfter pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="99853-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99853-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="99853-112">Section index:</span></span>  <br/> |<span data-ttu-id="99853-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="99853-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="99853-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="99853-114">Row index:</span></span>  <br/> |<span data-ttu-id="99853-115">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="99853-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="99853-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="99853-116">Cell index:</span></span>  <br/> |<span data-ttu-id="99853-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="99853-117">**visSpaceAfter**</span></span> <br/> |
   

