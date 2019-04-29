---
title: Célula ConFixedCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Determina quando um conector é redirecionado.
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404180"
---
# <a name="confixedcode-cell-shape-layout-section"></a><span data-ttu-id="18206-103">Célula ConFixedCode (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="18206-103">ConFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="18206-104">Determina quando um conector é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="18206-104">Determines when a connector reroutes.</span></span>
  
|<span data-ttu-id="18206-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="18206-105">**Value**</span></span>|<span data-ttu-id="18206-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18206-106">**Description**</span></span>|<span data-ttu-id="18206-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="18206-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18206-108">,0</span><span class="sxs-lookup"><span data-stu-id="18206-108">0</span></span>  <br/> |<span data-ttu-id="18206-109">Redirecionar livremente</span><span class="sxs-lookup"><span data-stu-id="18206-109">Reroute freely</span></span>  <br/> |<span data-ttu-id="18206-110">**visSLOConFixedRerouteFreely**</span><span class="sxs-lookup"><span data-stu-id="18206-110">**visSLOConFixedRerouteFreely**</span></span> <br/> |
|<span data-ttu-id="18206-111">1</span><span class="sxs-lookup"><span data-stu-id="18206-111">1</span></span>  <br/> |<span data-ttu-id="18206-112">Redirecionar conforme necessário (redirecionamento manual)</span><span class="sxs-lookup"><span data-stu-id="18206-112">Reroute as needed (manual reroute)</span></span>  <br/> |<span data-ttu-id="18206-113">**visSLOConFixedRerouteAsNeeded**</span><span class="sxs-lookup"><span data-stu-id="18206-113">**visSLOConFixedRerouteAsNeeded**</span></span> <br/> |
|<span data-ttu-id="18206-114">duas</span><span class="sxs-lookup"><span data-stu-id="18206-114">2</span></span>  <br/> |<span data-ttu-id="18206-115">Nunca redirecionar</span><span class="sxs-lookup"><span data-stu-id="18206-115">Never reroute</span></span>  <br/> |<span data-ttu-id="18206-116">**visSLOConFixedRerouteNever**</span><span class="sxs-lookup"><span data-stu-id="18206-116">**visSLOConFixedRerouteNever**</span></span> <br/> |
|<span data-ttu-id="18206-117">3D</span><span class="sxs-lookup"><span data-stu-id="18206-117">3</span></span>  <br/> |<span data-ttu-id="18206-118">Redirecionar ao cruzar</span><span class="sxs-lookup"><span data-stu-id="18206-118">Reroute on crossover</span></span>  <br/> |<span data-ttu-id="18206-119">**visSLOConFixedRerouteOnCrossover**</span><span class="sxs-lookup"><span data-stu-id="18206-119">**visSLOConFixedRerouteOnCrossover**</span></span> <br/> |
|<span data-ttu-id="18206-120">4 </span><span class="sxs-lookup"><span data-stu-id="18206-120">4</span></span>  <br/> |<span data-ttu-id="18206-121">Apenas para uso interno</span><span class="sxs-lookup"><span data-stu-id="18206-121">For internal use only</span></span>  <br/> |<span data-ttu-id="18206-122">**visSLOConFixedByAlgFrom**</span><span class="sxs-lookup"><span data-stu-id="18206-122">**visSLOConFixedByAlgFrom**</span></span> <br/> |
|<span data-ttu-id="18206-123">5 </span><span class="sxs-lookup"><span data-stu-id="18206-123">5</span></span>  <br/> |<span data-ttu-id="18206-124">Apenas para uso interno</span><span class="sxs-lookup"><span data-stu-id="18206-124">For internal use only</span></span>  <br/> |<span data-ttu-id="18206-125">**visSLOConFixedByAlgTo**</span><span class="sxs-lookup"><span data-stu-id="18206-125">**visSLOConFixedByAlgTo**</span></span> <br/> |
|<span data-ttu-id="18206-126">6 </span><span class="sxs-lookup"><span data-stu-id="18206-126">6</span></span>  <br/> |<span data-ttu-id="18206-127">Apenas para uso interno</span><span class="sxs-lookup"><span data-stu-id="18206-127">For internal use only</span></span>  <br/> |<span data-ttu-id="18206-128">**visSLOConFixedByAlgFromTo**</span><span class="sxs-lookup"><span data-stu-id="18206-128">**visSLOConFixedByAlgFromTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18206-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="18206-129">Remarks</span></span>

<span data-ttu-id="18206-130">Também é possível definir o valor desta célula selecionando um conector dinâmico, clicando em **Comportamento**, no grupo **Design da Forma**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **Conector**.</span><span class="sxs-lookup"><span data-stu-id="18206-130">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="18206-131">Para obter uma referência para a célula ConFixedCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="18206-131">To get a reference to the ConFixedCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18206-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="18206-132">Cell name:</span></span>  <br/> |<span data-ttu-id="18206-133">ConFixedCode</span><span class="sxs-lookup"><span data-stu-id="18206-133">ConFixedCode</span></span>  <br/> |
   
<span data-ttu-id="18206-134">Para obter uma referência para a célula ConFixedCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="18206-134">To get a reference to the ConFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18206-135">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="18206-135">Section index:</span></span>  <br/> |<span data-ttu-id="18206-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18206-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="18206-137">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="18206-137">Row index:</span></span>  <br/> |<span data-ttu-id="18206-138">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="18206-138">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="18206-139">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="18206-139">Cell index:</span></span>  <br/> |<span data-ttu-id="18206-140">**visSLOConFixedCode**</span><span class="sxs-lookup"><span data-stu-id="18206-140">**visSLOConFixedCode**</span></span> <br/> |
   

