---
title: Célula DisplayLevel (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Determina a faixa de níveis de exibição (o intervalo relativo do agrupamento da ordem Z) para a forma.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332533"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="7e65a-103">Célula DisplayLevel (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="7e65a-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="7e65a-104">Determina a faixa de níveis de exibição (o intervalo relativo do agrupamento da ordem Z) para a forma.</span><span class="sxs-lookup"><span data-stu-id="7e65a-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e65a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e65a-105">Remarks</span></span>

<span data-ttu-id="7e65a-p101">Ordem Z é a ordem de exibição das formas na página de desenho. Uma forma posicionada mais alto nessa ordem aparecerá na frente de uma forma que esteja mais baixo quando uma delas sobrepuser a outra.</span><span class="sxs-lookup"><span data-stu-id="7e65a-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="7e65a-p102">O nível de exibição divide as formas em agrupamentos (também conhecidos como faixas). Todas as formas em uma determinada faixa têm uma ordem Z mais alta que as existentes em uma faixa mais baixa. Por padrão, o nível de exibição da maioria das formas é zero (0).</span><span class="sxs-lookup"><span data-stu-id="7e65a-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="7e65a-p103">O intervalo de níveis de exibição varia de -32.767 a +32.767. Formas com o mesmo nível de exibição são combinadas em uma única faixa, dentro da qual também são classificadas em relação umas às outras pela ordem Z.</span><span class="sxs-lookup"><span data-stu-id="7e65a-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="7e65a-113">Você pode alterar a ordem Z das formas em uma banda usando os comandos **Avançar**, **Enviar para trás**, **trazer para frente**e **Enviar para trás**.</span><span class="sxs-lookup"><span data-stu-id="7e65a-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="7e65a-114">Se esses comandos moverem uma forma para fora da faixa determinada, o Microsoft Visio exibirá o valor reservado -32.768 na célula DisplayLevel da forma, a menos que a célula esteja protegida.</span><span class="sxs-lookup"><span data-stu-id="7e65a-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="7e65a-115">Nesse caso, a forma não poderá ser movida para outra faixa e o Visio exibirá o aviso "A proteção da forma e/ou as propriedades da camada impedem a execução completa deste comando".</span><span class="sxs-lookup"><span data-stu-id="7e65a-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="7e65a-116">Para obter uma referência à célula DisplayLevel pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7e65a-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e65a-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7e65a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="7e65a-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="7e65a-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="7e65a-119">Para obter uma referência à célula DisplayLevel pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7e65a-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e65a-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7e65a-120">Section index:</span></span>  <br/> |<span data-ttu-id="7e65a-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7e65a-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7e65a-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7e65a-122">Row index:</span></span>  <br/> |<span data-ttu-id="7e65a-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="7e65a-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="7e65a-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7e65a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="7e65a-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="7e65a-125">**visSLODisplayLevel**</span></span> <br/> |
   

