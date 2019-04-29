---
title: Célula ShapeFixedCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Especifica o comportamento de posicionamento de uma forma de colocação.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431740"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="36426-103">Célula ShapeFixedCode (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="36426-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="36426-104">Especifica o comportamento de posicionamento de uma forma de colocação.</span><span class="sxs-lookup"><span data-stu-id="36426-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="36426-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="36426-105">**Value**</span></span>|<span data-ttu-id="36426-106">**Modo de seleção**</span><span class="sxs-lookup"><span data-stu-id="36426-106">**Selection mode**</span></span>|<span data-ttu-id="36426-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="36426-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36426-108">&amp;Semestre</span><span class="sxs-lookup"><span data-stu-id="36426-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="36426-109">Não mover esta forma quando as formas forem projetadas usando a caixa de diálogo **Configurar layout** .</span><span class="sxs-lookup"><span data-stu-id="36426-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="36426-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="36426-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="36426-111">&amp;S2</span><span class="sxs-lookup"><span data-stu-id="36426-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="36426-112">Não mover esta forma e não permitir que as formas ajustadas sejam colocadas em cima dela.</span><span class="sxs-lookup"><span data-stu-id="36426-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="36426-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="36426-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="36426-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="36426-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="36426-115">Não mover esta forma e permitir que as formas ajustadas sejam colocadas em cima dela.</span><span class="sxs-lookup"><span data-stu-id="36426-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="36426-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="36426-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="36426-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="36426-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="36426-118">Ignorar localizações de ponto de conexão durante o roteamento.</span><span class="sxs-lookup"><span data-stu-id="36426-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="36426-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="36426-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="36426-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="36426-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="36426-121">Permitir somente o roteamento para lados com pontos de conexão.</span><span class="sxs-lookup"><span data-stu-id="36426-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="36426-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="36426-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="36426-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="36426-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="36426-124">Não associe ao perímetro desta forma.</span><span class="sxs-lookup"><span data-stu-id="36426-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="36426-125">Associe à caixa de alinhamento da forma.</span><span class="sxs-lookup"><span data-stu-id="36426-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="36426-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="36426-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36426-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="36426-127">Remarks</span></span>

<span data-ttu-id="36426-128">Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="36426-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="36426-129">Você pode definir qualquer combinação desses valores para a célula.</span><span class="sxs-lookup"><span data-stu-id="36426-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="36426-130">Por exemplo, você pode inserir o valor 3 (&amp;H3), que elimina o movimento ao dispor formas usando a caixa de diálogo **Configurar layout** (na guia **design** , no grupo **layout** , clique em refazer o **layout da página**e, em seguida, clique em \*\* Mais opções de layout\*\* ) e quando outras formas posicionáveis são colocadas na forma ou ao lado dela.</span><span class="sxs-lookup"><span data-stu-id="36426-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="36426-131">Nas versões do Visio anteriores ao Visio 2000, esse comportamento era definido por meio da célula ObjInteract na seção Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="36426-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="36426-132">Para obter uma referência à célula ShapeFixedCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize</span><span class="sxs-lookup"><span data-stu-id="36426-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36426-133">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="36426-133">Cell name:</span></span>  <br/> |<span data-ttu-id="36426-134">ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="36426-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="36426-135">Para obter uma referência para a célula ShapeFixedCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="36426-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36426-136">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="36426-136">Section index:</span></span>  <br/> |<span data-ttu-id="36426-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36426-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="36426-138">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="36426-138">Row index:</span></span>  <br/> |<span data-ttu-id="36426-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="36426-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="36426-140">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="36426-140">Cell index:</span></span>  <br/> |<span data-ttu-id="36426-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="36426-141">**visSLOFixedCode**</span></span> <br/> |
   

