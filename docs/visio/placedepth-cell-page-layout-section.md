---
title: Célula PlaceDepth (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Determina o tipo de layout e o método pelo qual o desenho é analisado antes de o layout ser criado.
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432034"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="b1140-103">Célula PlaceDepth (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="b1140-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="b1140-104">Determina o tipo de layout e o método pelo qual o desenho é analisado antes de o layout ser criado.</span><span class="sxs-lookup"><span data-stu-id="b1140-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="b1140-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b1140-105">**Value**</span></span>|<span data-ttu-id="b1140-106">**Profundidade do deslocamento para layouts verticais e horizontais**</span><span class="sxs-lookup"><span data-stu-id="b1140-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="b1140-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="b1140-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b1140-108">,0</span><span class="sxs-lookup"><span data-stu-id="b1140-108">0</span></span>  <br/> | <span data-ttu-id="b1140-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="b1140-109">Page default</span></span>  <br/> |<span data-ttu-id="b1140-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="b1140-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="b1140-111">1</span><span class="sxs-lookup"><span data-stu-id="b1140-111">1</span></span>  <br/> | <span data-ttu-id="b1140-112">Médio</span><span class="sxs-lookup"><span data-stu-id="b1140-112">Medium</span></span>  <br/> |<span data-ttu-id="b1140-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="b1140-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="b1140-114">duas</span><span class="sxs-lookup"><span data-stu-id="b1140-114">2</span></span>  <br/> | <span data-ttu-id="b1140-115">Detalhadas</span><span class="sxs-lookup"><span data-stu-id="b1140-115">Deep</span></span>  <br/> |<span data-ttu-id="b1140-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="b1140-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="b1140-117">3D</span><span class="sxs-lookup"><span data-stu-id="b1140-117">3</span></span>  <br/> | <span data-ttu-id="b1140-118">Superficial</span><span class="sxs-lookup"><span data-stu-id="b1140-118">Shallow</span></span>  <br/> |<span data-ttu-id="b1140-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="b1140-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1140-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1140-120">Remarks</span></span>

<span data-ttu-id="b1140-121">Para fazer referência à célula PlaceDepth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b1140-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1140-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b1140-122">Cell name:</span></span>  <br/> | <span data-ttu-id="b1140-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="b1140-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="b1140-124">Para fazer referência à célula PlaceDepth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b1140-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1140-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b1140-125">Section index:</span></span>  <br/> |<span data-ttu-id="b1140-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1140-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1140-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b1140-127">Row index:</span></span>  <br/> |<span data-ttu-id="b1140-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b1140-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="b1140-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b1140-129">Cell index:</span></span>  <br/> |<span data-ttu-id="b1140-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="b1140-130">**visPLOPlaceDepth**</span></span> <br/> |
   

