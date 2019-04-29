---
title: Célula ShapeSplittable (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indica se a forma 1D pode ser dividida.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427070"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="4897c-103">Célula ShapeSplittable (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="4897c-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="4897c-104">Indica se a forma 1D pode ser dividida.</span><span class="sxs-lookup"><span data-stu-id="4897c-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="4897c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4897c-105">**Value**</span></span>|<span data-ttu-id="4897c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4897c-106">**Description**</span></span>|<span data-ttu-id="4897c-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="4897c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4897c-108">,0</span><span class="sxs-lookup"><span data-stu-id="4897c-108">0</span></span>  <br/> | <span data-ttu-id="4897c-109">Não permitir a divisão desta forma.</span><span class="sxs-lookup"><span data-stu-id="4897c-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="4897c-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="4897c-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="4897c-111">1</span><span class="sxs-lookup"><span data-stu-id="4897c-111">1</span></span>  <br/> | <span data-ttu-id="4897c-112">Permitir a divisão desta forma.</span><span class="sxs-lookup"><span data-stu-id="4897c-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="4897c-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="4897c-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4897c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4897c-114">Remarks</span></span>

<span data-ttu-id="4897c-115">O comportamento padrão de conectores e outras formas 1D varia por tipo de desenho.</span><span class="sxs-lookup"><span data-stu-id="4897c-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="4897c-p101">A divisão automática de formas é habilitada e desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada nos níveis do aplicativo e da página.</span><span class="sxs-lookup"><span data-stu-id="4897c-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="4897c-118">Para habilitar ou desabilitar a divisão no nível do aplicativo, use a **configuração Habilitar divisão de conector** na guia **avançado** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , em **Opções**e em \*\* Avançado\*\* ).</span><span class="sxs-lookup"><span data-stu-id="4897c-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="4897c-119">Para habilitar ou desabilitar a divisão em uma página, consulte a célula [PageShapeSplit](pageshapesplit-cell-page-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="4897c-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="4897c-120">Para fazer com que uma forma possa dividir formas 1D divisíveis, consulte a célula [ShapeSplit](shapesplit-cell-shape-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="4897c-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="4897c-121">Para obter uma referência para a célula ShapeSplittable pelo nome, a partir de outra fórmula ou programa que use a \*\*\*\* propriedade Cells, utilize:</span><span class="sxs-lookup"><span data-stu-id="4897c-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4897c-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4897c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="4897c-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="4897c-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="4897c-124">Para fazer referência à célula ShapeSplittable pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4897c-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4897c-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4897c-125">Section index:</span></span>  <br/> |<span data-ttu-id="4897c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4897c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4897c-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="4897c-127">Row index:</span></span>  <br/> |<span data-ttu-id="4897c-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="4897c-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="4897c-129">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="4897c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="4897c-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="4897c-130">**visSLOSplittable**</span></span> <br/> |
   

