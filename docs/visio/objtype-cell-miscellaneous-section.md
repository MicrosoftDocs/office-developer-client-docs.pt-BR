---
title: Célula ObjType (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Determina se os objetos são de colocação ou se podem ser roteados em diagramas quando você usa a caixa de diálogo Configurar Layout para dispor formas.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425726"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="df0b5-103">Célula ObjType (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="df0b5-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="df0b5-104">Determina se os objetos são de colocação ou se podem ser roteados em diagramas quando você usa a caixa de diálogo **Configurar Layout** para dispor formas.</span><span class="sxs-lookup"><span data-stu-id="df0b5-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="df0b5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="df0b5-105">**Value**</span></span>|<span data-ttu-id="df0b5-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="df0b5-106">**Description**</span></span>|<span data-ttu-id="df0b5-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="df0b5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="df0b5-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="df0b5-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="df0b5-109">Padrão.</span><span class="sxs-lookup"><span data-stu-id="df0b5-109">Default.</span></span> <span data-ttu-id="df0b5-110">O aplicativo decide com base no contexto do desenho.</span><span class="sxs-lookup"><span data-stu-id="df0b5-110">The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="df0b5-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="df0b5-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="df0b5-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="df0b5-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="df0b5-113">A forma é de colocação.</span><span class="sxs-lookup"><span data-stu-id="df0b5-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="df0b5-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="df0b5-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="df0b5-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="df0b5-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="df0b5-116">A forma pode ser roteada.</span><span class="sxs-lookup"><span data-stu-id="df0b5-116">Shape is routable.</span></span> <span data-ttu-id="df0b5-117">Deve ser uma forma unidimensional (1D).</span><span class="sxs-lookup"><span data-stu-id="df0b5-117">Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="df0b5-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="df0b5-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="df0b5-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="df0b5-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="df0b5-120">A forma não é de colocação e não pode ser roteada.</span><span class="sxs-lookup"><span data-stu-id="df0b5-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="df0b5-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="df0b5-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="df0b5-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="df0b5-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="df0b5-123">O grupo contém formas de colocação e que podem ser roteadas.</span><span class="sxs-lookup"><span data-stu-id="df0b5-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="df0b5-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="df0b5-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df0b5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="df0b5-125">Remarks</span></span>

<span data-ttu-id="df0b5-p103">Como padrão, a célula ObjType está definida para uma forma como No Formula, cuja avaliação é 0, o que significa que o aplicativo irá determinar se a forma pode ser de colocação de acordo com seu contexto. Por exemplo, se você desenhar um simples retângulo, o valor de sua célula ObjType será 0. Em seguida, se você utilizar a ferramenta **Conector** para conectar o retângulo a outra forma, o Visio redefinirá o valor da célula ObjType do retângulo para 1 (de colocação).</span><span class="sxs-lookup"><span data-stu-id="df0b5-p103">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context. For example, if you draw a simple rectangle, the value of its ObjType cell is 0. If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="df0b5-129">O valor da célula ObjType pode ser uma combinação de valores.</span><span class="sxs-lookup"><span data-stu-id="df0b5-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="df0b5-130">Se o bit não placeable for definido ( H4), no entanto, ele tem precedência sobre outros valores, exceto o valor &amp; de grupo ( &amp; H8).</span><span class="sxs-lookup"><span data-stu-id="df0b5-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="df0b5-131">Para obter uma referência para a célula ObjType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="df0b5-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df0b5-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="df0b5-132">Cell name:</span></span>  <br/> |<span data-ttu-id="df0b5-133">ObjType</span><span class="sxs-lookup"><span data-stu-id="df0b5-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="df0b5-134">Para obter uma referência para a célula ObjType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="df0b5-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df0b5-135">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="df0b5-135">Section index:</span></span>  <br/> |<span data-ttu-id="df0b5-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df0b5-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="df0b5-137">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="df0b5-137">Row index:</span></span>  <br/> |<span data-ttu-id="df0b5-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="df0b5-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="df0b5-139">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="df0b5-139">Cell index:</span></span>  <br/> |<span data-ttu-id="df0b5-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="df0b5-140">**visLOFlags**</span></span> <br/> |
   

