---
title: Célula ConLineRouteExt (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Determina a aparência de um conector.
ms.openlocfilehash: 7724466b6ad225fcf39243bc80ba2e440f3b700b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771579"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="3297b-103">Célula ConLineRouteExt (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="3297b-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3297b-104">Determina a aparência de um conector.</span><span class="sxs-lookup"><span data-stu-id="3297b-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="3297b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3297b-105">**Value**</span></span>|<span data-ttu-id="3297b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3297b-106">**Description**</span></span>|<span data-ttu-id="3297b-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="3297b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3297b-108">0</span><span class="sxs-lookup"><span data-stu-id="3297b-108">0</span></span>  <br/> | <span data-ttu-id="3297b-109">Padrão; utiliza a configuração de página</span><span class="sxs-lookup"><span data-stu-id="3297b-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="3297b-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="3297b-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="3297b-111">1</span><span class="sxs-lookup"><span data-stu-id="3297b-111">1</span></span>  <br/> | <span data-ttu-id="3297b-112">Reto</span><span class="sxs-lookup"><span data-stu-id="3297b-112">Straight</span></span>  <br/> |<span data-ttu-id="3297b-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="3297b-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="3297b-114">2</span><span class="sxs-lookup"><span data-stu-id="3297b-114">2</span></span>  <br/> | <span data-ttu-id="3297b-115">Curvado</span><span class="sxs-lookup"><span data-stu-id="3297b-115">Curved</span></span>  <br/> |<span data-ttu-id="3297b-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="3297b-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3297b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3297b-117">Remarks</span></span>

<span data-ttu-id="3297b-118">Para fazer referência à célula ConLineRouteExt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3297b-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3297b-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3297b-119">Cell name:</span></span>  <br/> | <span data-ttu-id="3297b-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="3297b-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="3297b-121">Para fazer referência à célula ConLineRouteExt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3297b-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3297b-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3297b-122">Section index:</span></span>  <br/> |<span data-ttu-id="3297b-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3297b-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3297b-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="3297b-124">Row index:</span></span>  <br/> |<span data-ttu-id="3297b-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3297b-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="3297b-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3297b-126">Cell index:</span></span>  <br/> |<span data-ttu-id="3297b-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="3297b-127">**visSLOLineRouteExt**</span></span> <br/> |
   

