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
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434295"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="c26c3-103">Célula PlaceFlip (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="c26c3-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="c26c3-104">Determina como as formas de colocação são invertidas e/ou giradas em uma página quando a caixa de diálogo **Configurar Layout** é usada (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="c26c3-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="c26c3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c26c3-105">**Value**</span></span>|<span data-ttu-id="c26c3-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c26c3-106">**Description**</span></span>|<span data-ttu-id="c26c3-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="c26c3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c26c3-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="c26c3-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="c26c3-109">Padrão.</span><span class="sxs-lookup"><span data-stu-id="c26c3-109">Default.</span></span> <span data-ttu-id="c26c3-110">Não inverter.</span><span class="sxs-lookup"><span data-stu-id="c26c3-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="c26c3-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="c26c3-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="c26c3-112">&amp;Semestre</span><span class="sxs-lookup"><span data-stu-id="c26c3-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="c26c3-113">Inverter horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c26c3-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="c26c3-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="c26c3-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="c26c3-115">&amp;S2</span><span class="sxs-lookup"><span data-stu-id="c26c3-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="c26c3-116">Inverter verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c26c3-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="c26c3-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="c26c3-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="c26c3-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="c26c3-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="c26c3-119">Inverter em incrementos de 90 graus.</span><span class="sxs-lookup"><span data-stu-id="c26c3-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="c26c3-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="c26c3-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="c26c3-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="c26c3-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="c26c3-122">Não inverter.</span><span class="sxs-lookup"><span data-stu-id="c26c3-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="c26c3-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="c26c3-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c26c3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c26c3-124">Remarks</span></span>

<span data-ttu-id="c26c3-p102">O valor na célula PlaceFlip ajuda a orientar uma forma de colocação em direção à próxima forma de colocação à qual está conectada. É utilizado normalmente ao dispor os desenhos que utilizam a cola estática.</span><span class="sxs-lookup"><span data-stu-id="c26c3-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="c26c3-127">Para definir esse comportamento para uma determinada forma, utilize a célula ShapePlaceFlip na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="c26c3-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="c26c3-128">Para obter uma referência à célula PlaceFlip pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c26c3-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c26c3-129">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c26c3-129">Cell name:</span></span>  <br/> |<span data-ttu-id="c26c3-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="c26c3-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="c26c3-131">Para obter uma referência para a célula PlaceFlip pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c26c3-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c26c3-132">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c26c3-132">Section index:</span></span>  <br/> |<span data-ttu-id="c26c3-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c26c3-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c26c3-134">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c26c3-134">Row index:</span></span>  <br/> |<span data-ttu-id="c26c3-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c26c3-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="c26c3-136">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c26c3-136">Cell index:</span></span>  <br/> |<span data-ttu-id="c26c3-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="c26c3-137">**visPLOPlaceFlip**</span></span> <br/> |
   

