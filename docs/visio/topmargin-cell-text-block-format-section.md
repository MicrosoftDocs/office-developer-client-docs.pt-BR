---
title: Célula TopMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1015
localization_priority: Normal
ms.assetid: c599b444-4d0e-a855-b04b-dd9dcaedf263
description: Determina a distância entre a borda superior do bloco de texto e a primeira linha do texto. O padrão é 4,0000 ponto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem superior será a mesma.
ms.openlocfilehash: 97d349fd4ddc3c76cda61e1ee7ce25909161e6fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435569"
---
# <a name="topmargin-cell-text-block-format-section"></a><span data-ttu-id="8010b-106">Célula TopMargin (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="8010b-106">TopMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="8010b-p102">Determina a distância entre a borda superior do bloco de texto e a primeira linha do texto. O padrão é 4,0000 ponto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem superior será a mesma.</span><span class="sxs-lookup"><span data-stu-id="8010b-p102">Determines the distance between the top border of the text block and the first line of text it contains. The default is 4.0000 point. This value is independent of the scale of the drawing. If the drawing is scaled, the top margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8010b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8010b-111">Remarks</span></span>

<span data-ttu-id="8010b-112">Para fazer referência à célula TopMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8010b-112">To get a reference to the TopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8010b-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8010b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8010b-114">TopMargin</span><span class="sxs-lookup"><span data-stu-id="8010b-114">TopMargin</span></span>  <br/> |
   
<span data-ttu-id="8010b-115">Para fazer referência à célula TopMargin pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8010b-115">To get a reference to the TopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8010b-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8010b-116">Section index:</span></span>  <br/> |<span data-ttu-id="8010b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8010b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8010b-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="8010b-118">Row index:</span></span>  <br/> |<span data-ttu-id="8010b-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="8010b-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="8010b-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8010b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8010b-121">**visTxtBlkTopMargin**</span><span class="sxs-lookup"><span data-stu-id="8010b-121">**visTxtBlkTopMargin**</span></span> <br/> |
   

