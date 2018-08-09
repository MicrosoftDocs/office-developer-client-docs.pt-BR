---
title: Célula DropOnPageScale (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771764"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="743d7-102">Célula DropOnPageScale (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="743d7-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="743d7-103">Contém o percentual da escala de uma forma quando colocada na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="743d7-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="743d7-104">Comentários</span><span class="sxs-lookup"><span data-stu-id="743d7-104">Remarks</span></span>

<span data-ttu-id="743d7-105">Nos seguintes casos, o Visio coloca as formas em escala para que apareçam adequadamente na página de desenho:</span><span class="sxs-lookup"><span data-stu-id="743d7-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="743d7-106">Quando formas sem medida são colocadas em desenhos com escala.</span><span class="sxs-lookup"><span data-stu-id="743d7-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="743d7-107">Quando formas com medida são colocadas em desenhos sem escala.</span><span class="sxs-lookup"><span data-stu-id="743d7-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="743d7-108">O percentual da célula DropOnPageScale indica o fator pelo qual o Visio dimensionado de forma, acima (\>100) ou para baixo (\<100).</span><span class="sxs-lookup"><span data-stu-id="743d7-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="743d7-109">Você pode usar esse número como um fator ao calcular valores codificados.</span><span class="sxs-lookup"><span data-stu-id="743d7-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="743d7-110">Esse valor é 100% para formas com medida em desenhos com escala ou formas sem medida em desenhos sem escala.</span><span class="sxs-lookup"><span data-stu-id="743d7-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="743d7-111">Para fazer referência à célula DropOnPageScale pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="743d7-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="743d7-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="743d7-112">Cell name:</span></span>  <br/> | <span data-ttu-id="743d7-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="743d7-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="743d7-114">Para fazer referência à célula DropOnPageScale pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="743d7-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="743d7-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="743d7-115">Section index:</span></span>  <br/> |<span data-ttu-id="743d7-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="743d7-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="743d7-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="743d7-117">Row index:</span></span>  <br/> |<span data-ttu-id="743d7-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="743d7-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="743d7-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="743d7-119">Cell index:</span></span>  <br/> |<span data-ttu-id="743d7-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="743d7-120">**visObjDropOnPageScale**</span></span> <br/> |
   

