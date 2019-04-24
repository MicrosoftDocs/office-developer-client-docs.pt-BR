---
title: Célula ShapePlaceFlip (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Determina como as formas de colocação são invertidas, giradas, ou ambos, na página ao dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332666"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="49d71-103">Célula ShapePlaceFlip (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="49d71-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="49d71-104">Determina como as formas de colocação são invertidas, giradas, ou ambos, na página ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="49d71-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="49d71-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="49d71-105">**Value**</span></span>|<span data-ttu-id="49d71-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="49d71-106">**Description**</span></span>|<span data-ttu-id="49d71-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="49d71-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="49d71-108">,0</span><span class="sxs-lookup"><span data-stu-id="49d71-108">0</span></span>  <br/> |<span data-ttu-id="49d71-109">Utilizar padrão de página.</span><span class="sxs-lookup"><span data-stu-id="49d71-109">Use page default.</span></span>  <br/> |<span data-ttu-id="49d71-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="49d71-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="49d71-111">1</span><span class="sxs-lookup"><span data-stu-id="49d71-111">1</span></span>  <br/> |<span data-ttu-id="49d71-112">Inverter horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="49d71-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="49d71-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="49d71-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="49d71-114">duas</span><span class="sxs-lookup"><span data-stu-id="49d71-114">2</span></span>  <br/> |<span data-ttu-id="49d71-115">Inverter verticalmente.</span><span class="sxs-lookup"><span data-stu-id="49d71-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="49d71-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="49d71-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="49d71-117">quatro</span><span class="sxs-lookup"><span data-stu-id="49d71-117">4</span></span>  <br/> |<span data-ttu-id="49d71-118">Inverter em incrementos de 90 graus entre 0 e 270.</span><span class="sxs-lookup"><span data-stu-id="49d71-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="49d71-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="49d71-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="49d71-120">8</span><span class="sxs-lookup"><span data-stu-id="49d71-120">8</span></span>  <br/> |<span data-ttu-id="49d71-121">Não inverter.</span><span class="sxs-lookup"><span data-stu-id="49d71-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="49d71-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="49d71-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49d71-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="49d71-123">Remarks</span></span>

<span data-ttu-id="49d71-124">O valor na célula ShapePlaceFlip ajuda a orientar uma forma de colocação em direção à próxima forma de colocação à qual está conectada.</span><span class="sxs-lookup"><span data-stu-id="49d71-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="49d71-125">Para definir esse comportamento para *todas* as formas na página de desenho, use a célula PlaceFlip na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="49d71-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="49d71-126">Para obter uma referência para a célula ShapePlaceFlip pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="49d71-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49d71-127">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="49d71-127">Cell name:</span></span>  <br/> |<span data-ttu-id="49d71-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="49d71-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="49d71-129">Para obter uma referência para a célula ShapePlaceFlip pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="49d71-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49d71-130">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="49d71-130">Section index:</span></span>  <br/> |<span data-ttu-id="49d71-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="49d71-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="49d71-132">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="49d71-132">Row index:</span></span>  <br/> |<span data-ttu-id="49d71-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="49d71-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="49d71-134">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="49d71-134">Cell index:</span></span>  <br/> |<span data-ttu-id="49d71-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="49d71-135">**visSLOPlaceFlip**</span></span> <br/> |
   

