---
title: Célula PlaceFlip (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Determina como as formas de colocação são invertidas e/ou giradas em uma página quando a caixa de diálogo Configurar Layout é usada (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: fb16849c7a496a4277133c68453d94d6fd2e67f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772483"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="cb03b-103">Célula PlaceFlip (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="cb03b-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="cb03b-104">Determina como as formas de colocação são invertidas e/ou giradas em uma página quando a caixa de diálogo **Configurar Layout** é usada (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="cb03b-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="cb03b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb03b-105">**Value**</span></span>|<span data-ttu-id="cb03b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cb03b-106">**Description**</span></span>|<span data-ttu-id="cb03b-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="cb03b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb03b-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="cb03b-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="cb03b-p101">Padrão. Não inverter.</span><span class="sxs-lookup"><span data-stu-id="cb03b-p101">Default. Do not flip.</span></span>  <br/> |<span data-ttu-id="cb03b-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="cb03b-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="cb03b-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="cb03b-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="cb03b-113">Inverter horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="cb03b-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="cb03b-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="cb03b-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="cb03b-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="cb03b-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="cb03b-116">Inverter verticalmente.</span><span class="sxs-lookup"><span data-stu-id="cb03b-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="cb03b-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="cb03b-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="cb03b-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="cb03b-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="cb03b-119">Inverter em incrementos de 90 graus.</span><span class="sxs-lookup"><span data-stu-id="cb03b-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="cb03b-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="cb03b-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="cb03b-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="cb03b-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="cb03b-122">Não inverter.</span><span class="sxs-lookup"><span data-stu-id="cb03b-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="cb03b-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="cb03b-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb03b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb03b-124">Remarks</span></span>

<span data-ttu-id="cb03b-p102">O valor na célula PlaceFlip ajuda a orientar uma forma de colocação em direção à próxima forma de colocação à qual está conectada. É utilizado normalmente ao dispor os desenhos que utilizam a cola estática.</span><span class="sxs-lookup"><span data-stu-id="cb03b-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="cb03b-127">Para definir esse comportamento para uma determinada forma, utilize a célula ShapePlaceFlip na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="cb03b-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="cb03b-128">Para obter uma referência à célula PlaceFlip pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cb03b-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb03b-129">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cb03b-129">Cell name:</span></span>  <br/> |<span data-ttu-id="cb03b-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="cb03b-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="cb03b-131">Para obter uma referência para a célula PlaceFlip pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cb03b-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb03b-132">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cb03b-132">Section index:</span></span>  <br/> |<span data-ttu-id="cb03b-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb03b-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cb03b-134">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cb03b-134">Row index:</span></span>  <br/> |<span data-ttu-id="cb03b-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="cb03b-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="cb03b-136">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cb03b-136">Cell index:</span></span>  <br/> |<span data-ttu-id="cb03b-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="cb03b-137">**visPLOPlaceFlip**</span></span> <br/> |
   

