---
title: Célula LineRouteExt (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Determina a aparência padrão de todos os conectores em uma página de desenho.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358979"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="cb7fa-103">Célula LineRouteExt (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="cb7fa-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="cb7fa-104">Determina a aparência padrão de todos os conectores em uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="cb7fa-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-105">**Value**</span></span>|<span data-ttu-id="cb7fa-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-106">**Description**</span></span>|<span data-ttu-id="cb7fa-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="cb7fa-108">,0</span><span class="sxs-lookup"><span data-stu-id="cb7fa-108">0</span></span>  <br/> | <span data-ttu-id="cb7fa-109">Padrão (reto)</span><span class="sxs-lookup"><span data-stu-id="cb7fa-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="cb7fa-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="cb7fa-111">1</span><span class="sxs-lookup"><span data-stu-id="cb7fa-111">1</span></span>  <br/> | <span data-ttu-id="cb7fa-112">Estreita</span><span class="sxs-lookup"><span data-stu-id="cb7fa-112">Straight</span></span>  <br/> |<span data-ttu-id="cb7fa-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="cb7fa-114">duas</span><span class="sxs-lookup"><span data-stu-id="cb7fa-114">2</span></span>  <br/> | <span data-ttu-id="cb7fa-115">Curvo</span><span class="sxs-lookup"><span data-stu-id="cb7fa-115">Curved</span></span>  <br/> |<span data-ttu-id="cb7fa-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb7fa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb7fa-117">Remarks</span></span>

<span data-ttu-id="cb7fa-118">Para fazer referência à célula LineRouteExt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cb7fa-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb7fa-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cb7fa-119">Cell name:</span></span>  <br/> | <span data-ttu-id="cb7fa-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="cb7fa-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="cb7fa-121">Para fazer referência à célula LineRouteExt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cb7fa-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb7fa-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cb7fa-122">Section index:</span></span>  <br/> |<span data-ttu-id="cb7fa-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cb7fa-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cb7fa-124">Row index:</span></span>  <br/> |<span data-ttu-id="cb7fa-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="cb7fa-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cb7fa-126">Cell index:</span></span>  <br/> |<span data-ttu-id="cb7fa-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="cb7fa-127">**visPLOLineRouteExt**</span></span> <br/> |
   

