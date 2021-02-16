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
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="8c738-103">Célula PlaceDepth (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="8c738-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="8c738-104">Determina o tipo de layout e o método pelo qual o desenho é analisado antes de o layout ser criado.</span><span class="sxs-lookup"><span data-stu-id="8c738-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="8c738-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8c738-105">**Value**</span></span>|<span data-ttu-id="8c738-106">**Profundidade do deslocamento para layouts verticais e horizontais**</span><span class="sxs-lookup"><span data-stu-id="8c738-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="8c738-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="8c738-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8c738-108">0</span><span class="sxs-lookup"><span data-stu-id="8c738-108">0</span></span>  <br/> | <span data-ttu-id="8c738-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="8c738-109">Page default</span></span>  <br/> |<span data-ttu-id="8c738-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="8c738-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="8c738-111">1 </span><span class="sxs-lookup"><span data-stu-id="8c738-111">1</span></span>  <br/> | <span data-ttu-id="8c738-112">Médio</span><span class="sxs-lookup"><span data-stu-id="8c738-112">Medium</span></span>  <br/> |<span data-ttu-id="8c738-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="8c738-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="8c738-114">2 </span><span class="sxs-lookup"><span data-stu-id="8c738-114">2</span></span>  <br/> | <span data-ttu-id="8c738-115">Profundidade</span><span class="sxs-lookup"><span data-stu-id="8c738-115">Deep</span></span>  <br/> |<span data-ttu-id="8c738-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="8c738-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="8c738-117">3 </span><span class="sxs-lookup"><span data-stu-id="8c738-117">3</span></span>  <br/> | <span data-ttu-id="8c738-118">Superficial</span><span class="sxs-lookup"><span data-stu-id="8c738-118">Shallow</span></span>  <br/> |<span data-ttu-id="8c738-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="8c738-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c738-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c738-120">Remarks</span></span>

<span data-ttu-id="8c738-121">Para fazer referência à célula PlaceDepth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8c738-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c738-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8c738-122">Cell name:</span></span>  <br/> | <span data-ttu-id="8c738-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="8c738-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="8c738-124">Para fazer referência à célula PlaceDepth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8c738-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c738-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8c738-125">Section index:</span></span>  <br/> |<span data-ttu-id="8c738-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c738-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8c738-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="8c738-127">Row index:</span></span>  <br/> |<span data-ttu-id="8c738-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8c738-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="8c738-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8c738-129">Cell index:</span></span>  <br/> |<span data-ttu-id="8c738-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="8c738-130">**visPLOPlaceDepth**</span></span> <br/> |
   

