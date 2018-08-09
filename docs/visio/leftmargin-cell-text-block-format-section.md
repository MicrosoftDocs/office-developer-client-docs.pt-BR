---
title: Célula LeftMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Determina a distância entre a borda esquerda do bloco de texto e o texto contido nele. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem esquerda será a mesma.
ms.openlocfilehash: d24ba33bffea1529490b49e105fec5d01cd828b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772177"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="febea-106">Célula LeftMargin (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="febea-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="febea-p102">Determina a distância entre a borda esquerda do bloco de texto e o texto contido nele. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem esquerda será a mesma.</span><span class="sxs-lookup"><span data-stu-id="febea-p102">Determines the distance between the left border of the text block and the text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="febea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="febea-111">Remarks</span></span>

<span data-ttu-id="febea-112">Para fazer referência à célula LeftMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="febea-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="febea-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="febea-113">Cell name:</span></span>  <br/> | <span data-ttu-id="febea-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="febea-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="febea-115">Para fazer referência à célula LeftMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="febea-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="febea-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="febea-116">Section index:</span></span>  <br/> |<span data-ttu-id="febea-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="febea-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="febea-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="febea-118">Row index:</span></span>  <br/> |<span data-ttu-id="febea-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="febea-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="febea-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="febea-120">Cell index:</span></span>  <br/> |<span data-ttu-id="febea-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="febea-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

