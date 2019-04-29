---
title: Célula PageShapeSplit (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indica se as formas na página podem ser divididas automaticamente.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422016"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="79c46-103">Célula PageShapeSplit (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="79c46-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="79c46-104">Indica se as formas na página podem ser divididas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="79c46-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="79c46-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="79c46-105">**Value**</span></span>|<span data-ttu-id="79c46-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="79c46-106">**Description**</span></span>|<span data-ttu-id="79c46-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="79c46-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79c46-108">,0</span><span class="sxs-lookup"><span data-stu-id="79c46-108">0</span></span>  <br/> |<span data-ttu-id="79c46-109">Não permite divisão automática de forma.</span><span class="sxs-lookup"><span data-stu-id="79c46-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="79c46-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="79c46-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="79c46-111">1</span><span class="sxs-lookup"><span data-stu-id="79c46-111">1</span></span>  <br/> |<span data-ttu-id="79c46-112">Permite divisão automática de forma (padrão).</span><span class="sxs-lookup"><span data-stu-id="79c46-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="79c46-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="79c46-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79c46-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="79c46-114">Remarks</span></span>

<span data-ttu-id="79c46-p101">A divisão automática de formas é habilitada ou desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada no aplicativo e na página. A configuração padrão para formas varia por tipo de desenho.</span><span class="sxs-lookup"><span data-stu-id="79c46-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="79c46-118">Para habilitar ou desabilitar a divisão no nível do aplicativo, use a **configuração Habilitar divisão de conector** na guia **avançado** da caixa de diálogo **Opções do Visio** (clique no botão **Office** , em **Opções** no **Visio** e, em seguida, clique em **avançado** .</span><span class="sxs-lookup"><span data-stu-id="79c46-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="79c46-119">Para habilitar ou desabilitar a divisão no nível da forma, consulte as células ShapeSplit e ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="79c46-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="79c46-120">Para obter uma referência para a célula PageShapeSplit pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="79c46-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79c46-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="79c46-121">Cell name:</span></span>  <br/> |<span data-ttu-id="79c46-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="79c46-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="79c46-123">Para obter uma referência para a célula PageShapeSplit pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="79c46-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79c46-124">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="79c46-124">Section index:</span></span>  <br/> |<span data-ttu-id="79c46-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="79c46-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="79c46-126">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="79c46-126">Row index:</span></span>  <br/> |<span data-ttu-id="79c46-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="79c46-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="79c46-128">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="79c46-128">Cell index:</span></span>  <br/> |<span data-ttu-id="79c46-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="79c46-129">**visPLOSplit**</span></span> <br/> |
   

