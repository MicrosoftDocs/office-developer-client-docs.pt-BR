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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346792"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="d1f0d-103">Célula PlaceDepth (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="d1f0d-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="d1f0d-104">Determina o tipo de layout e o método pelo qual o desenho é analisado antes de o layout ser criado.</span><span class="sxs-lookup"><span data-stu-id="d1f0d-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="d1f0d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-105">**Value**</span></span>|<span data-ttu-id="d1f0d-106">**Profundidade do deslocamento para layouts verticais e horizontais**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="d1f0d-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d1f0d-108">,0</span><span class="sxs-lookup"><span data-stu-id="d1f0d-108">0</span></span>  <br/> | <span data-ttu-id="d1f0d-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="d1f0d-109">Page default</span></span>  <br/> |<span data-ttu-id="d1f0d-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="d1f0d-111">1</span><span class="sxs-lookup"><span data-stu-id="d1f0d-111">1</span></span>  <br/> | <span data-ttu-id="d1f0d-112">Médio</span><span class="sxs-lookup"><span data-stu-id="d1f0d-112">Medium</span></span>  <br/> |<span data-ttu-id="d1f0d-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="d1f0d-114">duas</span><span class="sxs-lookup"><span data-stu-id="d1f0d-114">2</span></span>  <br/> | <span data-ttu-id="d1f0d-115">Detalhadas</span><span class="sxs-lookup"><span data-stu-id="d1f0d-115">Deep</span></span>  <br/> |<span data-ttu-id="d1f0d-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="d1f0d-117">3D</span><span class="sxs-lookup"><span data-stu-id="d1f0d-117">3</span></span>  <br/> | <span data-ttu-id="d1f0d-118">Superficial</span><span class="sxs-lookup"><span data-stu-id="d1f0d-118">Shallow</span></span>  <br/> |<span data-ttu-id="d1f0d-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1f0d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1f0d-120">Remarks</span></span>

<span data-ttu-id="d1f0d-121">Para fazer referência à célula PlaceDepth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d1f0d-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1f0d-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d1f0d-122">Cell name:</span></span>  <br/> | <span data-ttu-id="d1f0d-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="d1f0d-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="d1f0d-124">Para fazer referência à célula PlaceDepth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d1f0d-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1f0d-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d1f0d-125">Section index:</span></span>  <br/> |<span data-ttu-id="d1f0d-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d1f0d-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d1f0d-127">Row index:</span></span>  <br/> |<span data-ttu-id="d1f0d-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="d1f0d-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d1f0d-129">Cell index:</span></span>  <br/> |<span data-ttu-id="d1f0d-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="d1f0d-130">**visPLOPlaceDepth**</span></span> <br/> |
   

