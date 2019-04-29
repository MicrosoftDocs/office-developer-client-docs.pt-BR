---
title: Célula ShapeSplit (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indica se esta forma pode dividir formas que sejam divisíveis.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423556"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="52a7a-103">Célula ShapeSplit (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="52a7a-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="52a7a-104">Indica se esta forma pode dividir formas que sejam divisíveis.</span><span class="sxs-lookup"><span data-stu-id="52a7a-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="52a7a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="52a7a-105">**Value**</span></span>|<span data-ttu-id="52a7a-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52a7a-106">**Description**</span></span>|<span data-ttu-id="52a7a-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="52a7a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="52a7a-108">,0</span><span class="sxs-lookup"><span data-stu-id="52a7a-108">0</span></span>  <br/> | <span data-ttu-id="52a7a-109">Não permitir que esta forma divida outras formas.</span><span class="sxs-lookup"><span data-stu-id="52a7a-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="52a7a-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="52a7a-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="52a7a-111">1</span><span class="sxs-lookup"><span data-stu-id="52a7a-111">1</span></span>  <br/> | <span data-ttu-id="52a7a-112">Permitir que esta forma divida outras formas.</span><span class="sxs-lookup"><span data-stu-id="52a7a-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="52a7a-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="52a7a-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52a7a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="52a7a-114">Remarks</span></span>

<span data-ttu-id="52a7a-115">Uma forma que divide outras formas deve ser uma forma 2D ou uma forma de colocação 1D.</span><span class="sxs-lookup"><span data-stu-id="52a7a-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="52a7a-p101">A divisão automática de formas é habilitada e desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada no nível do aplicativo e da página; nas formas, ela varia por tipo de desenho.</span><span class="sxs-lookup"><span data-stu-id="52a7a-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="52a7a-118">Para habilitar ou desabilitar a divisão no nível do aplicativo, use a **configuração Habilitar divisão de conector** na guia **avançado** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , em **Opções**e em \*\* Avançado\*\*).</span><span class="sxs-lookup"><span data-stu-id="52a7a-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="52a7a-119">Para habilitar ou desabilitar a divisão em uma página, consulte a célula PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="52a7a-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="52a7a-120">Para fazer com que uma forma 1D possa ser dividida, consulte a célula ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="52a7a-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="52a7a-121">Para obter uma referência para a célula ShapeSplit pelo nome, a partir de outra fórmula ou programa que use a \*\*\*\* propriedade Cells, utilize:</span><span class="sxs-lookup"><span data-stu-id="52a7a-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52a7a-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="52a7a-122">Cell name:</span></span>  <br/> | <span data-ttu-id="52a7a-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="52a7a-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="52a7a-124">Para fazer referência à célula ShapeSplit pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="52a7a-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52a7a-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="52a7a-125">Section index:</span></span>  <br/> |<span data-ttu-id="52a7a-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52a7a-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="52a7a-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="52a7a-127">Row index:</span></span>  <br/> |<span data-ttu-id="52a7a-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="52a7a-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="52a7a-129">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="52a7a-129">Cell index:</span></span>  <br/> |<span data-ttu-id="52a7a-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="52a7a-130">**visSLOSplit**</span></span> <br/> |
   

