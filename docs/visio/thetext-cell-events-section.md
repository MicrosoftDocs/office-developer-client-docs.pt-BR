---
title: Célula TheText (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Uma célula de evento avaliada quando a composição do texto ou o texto da forma é alterado.
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773140"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="b7485-103">Célula TheText (Seção Events)</span><span class="sxs-lookup"><span data-stu-id="b7485-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="b7485-104">Uma célula de evento avaliada quando a composição do texto ou o texto da forma é alterado.</span><span class="sxs-lookup"><span data-stu-id="b7485-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7485-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7485-105">Remarks</span></span>

<span data-ttu-id="b7485-p101">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula. É possível utilizar a célula TheText para disparar recálculos, por exemplo, recalcular a largura e a altura do texto com as funções TEXTWIDTH( ) e TEXTHEIGHT( ).</span><span class="sxs-lookup"><span data-stu-id="b7485-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="b7485-108">Para fazer referência à célula TheText pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b7485-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7485-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b7485-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b7485-110">TheText</span><span class="sxs-lookup"><span data-stu-id="b7485-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="b7485-111">Para fazer referência à célula TheText pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b7485-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7485-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b7485-112">Section index:</span></span>  <br/> |<span data-ttu-id="b7485-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b7485-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b7485-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b7485-114">Row index:</span></span>  <br/> |<span data-ttu-id="b7485-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="b7485-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="b7485-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b7485-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b7485-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="b7485-117">**visEvtCellTheText**</span></span> <br/> |
   

