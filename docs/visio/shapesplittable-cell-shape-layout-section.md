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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349151"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="39ba9-103">Célula ShapeSplittable (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="39ba9-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="39ba9-104">Indica se a forma 1D pode ser dividida.</span><span class="sxs-lookup"><span data-stu-id="39ba9-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="39ba9-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="39ba9-105">**Value**</span></span>|<span data-ttu-id="39ba9-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39ba9-106">**Description**</span></span>|<span data-ttu-id="39ba9-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="39ba9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="39ba9-108">,0</span><span class="sxs-lookup"><span data-stu-id="39ba9-108">0</span></span>  <br/> | <span data-ttu-id="39ba9-109">Não permitir a divisão desta forma.</span><span class="sxs-lookup"><span data-stu-id="39ba9-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="39ba9-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="39ba9-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="39ba9-111">1</span><span class="sxs-lookup"><span data-stu-id="39ba9-111">1</span></span>  <br/> | <span data-ttu-id="39ba9-112">Permitir a divisão desta forma.</span><span class="sxs-lookup"><span data-stu-id="39ba9-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="39ba9-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="39ba9-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39ba9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="39ba9-114">Remarks</span></span>

<span data-ttu-id="39ba9-115">O comportamento padrão de conectores e outras formas 1D varia por tipo de desenho.</span><span class="sxs-lookup"><span data-stu-id="39ba9-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="39ba9-p101">A divisão automática de formas é habilitada e desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada nos níveis do aplicativo e da página.</span><span class="sxs-lookup"><span data-stu-id="39ba9-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="39ba9-118">Para habilitar ou desabilitar a divisão no nível do aplicativo, use a **configuração Habilitar divisão de conector** na guia **avançado** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , em **Opções**e em \*\* Avançado\*\* ).</span><span class="sxs-lookup"><span data-stu-id="39ba9-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="39ba9-119">Para habilitar ou desabilitar a divisão em uma página, consulte a célula [PageShapeSplit](pageshapesplit-cell-page-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="39ba9-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="39ba9-120">Para fazer com que uma forma possa dividir formas 1D divisíveis, consulte a célula [ShapeSplit](shapesplit-cell-shape-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="39ba9-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="39ba9-121">Para obter uma referência para a célula ShapeSplittable pelo nome, a partir de outra fórmula ou programa que use a \*\*\*\* propriedade Cells, utilize:</span><span class="sxs-lookup"><span data-stu-id="39ba9-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39ba9-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="39ba9-122">Cell name:</span></span>  <br/> | <span data-ttu-id="39ba9-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="39ba9-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="39ba9-124">Para fazer referência à célula ShapeSplittable pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="39ba9-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39ba9-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="39ba9-125">Section index:</span></span>  <br/> |<span data-ttu-id="39ba9-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="39ba9-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="39ba9-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="39ba9-127">Row index:</span></span>  <br/> |<span data-ttu-id="39ba9-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="39ba9-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="39ba9-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="39ba9-129">Cell index:</span></span>  <br/> |<span data-ttu-id="39ba9-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="39ba9-130">**visSLOSplittable**</span></span> <br/> |
   

