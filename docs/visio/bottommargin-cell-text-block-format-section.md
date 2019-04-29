---
title: Célula BottomMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: Determina a distância entre a borda inferior do bloco de texto e a última linha do texto. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem inferior será a mesma.
ms.openlocfilehash: 544557f1e797315619bc9975db0b87a09981726c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417207"
---
# <a name="bottommargin-cell-text-block-format-section"></a><span data-ttu-id="b53a4-106">Célula BottomMargin (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="b53a4-106">BottomMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="b53a4-p102">Determina a distância entre a borda inferior do bloco de texto e a última linha do texto. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem inferior será a mesma.</span><span class="sxs-lookup"><span data-stu-id="b53a4-p102">Determines the distance between the bottom border of the text block and the last line of text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the bottom margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b53a4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b53a4-111">Remarks</span></span>

<span data-ttu-id="b53a4-112">Para fazer referência à célula BottomMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b53a4-112">To get a reference to the BottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b53a4-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b53a4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b53a4-114">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="b53a4-114">BottomMargin</span></span>  <br/> |
   
<span data-ttu-id="b53a4-115">Para fazer referência à célula BottomMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b53a4-115">To get a reference to the BottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b53a4-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b53a4-116">Section index:</span></span>  <br/> |<span data-ttu-id="b53a4-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b53a4-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b53a4-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b53a4-118">Row index:</span></span>  <br/> |<span data-ttu-id="b53a4-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="b53a4-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="b53a4-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b53a4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b53a4-121">**visTxtBlkBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="b53a4-121">**visTxtBlkBottomMargin**</span></span> <br/> |
   

