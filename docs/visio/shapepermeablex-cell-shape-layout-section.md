---
title: Célula ShapePermeableX (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Determina se um conector pode fazer o roteamento horizontalmente por uma forma de colocação.
ms.openlocfilehash: 1e0fe614b9401ea453b9c650ef9af3b4105b3805
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772893"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="4ca68-103">Célula ShapePermeableX (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="4ca68-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="4ca68-104">Determina se um conector pode fazer o roteamento horizontalmente por uma forma de colocação.</span><span class="sxs-lookup"><span data-stu-id="4ca68-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="4ca68-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4ca68-105">**Value**</span></span>|<span data-ttu-id="4ca68-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4ca68-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ca68-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="4ca68-107">TRUE</span></span>  <br/> |<span data-ttu-id="4ca68-108">Permitir que os conectores façam o roteamento horizontalmente por uma forma de colocação.</span><span class="sxs-lookup"><span data-stu-id="4ca68-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="4ca68-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="4ca68-109">FALSE</span></span>  <br/> |<span data-ttu-id="4ca68-110">Não permitir que os conectores façam o roteamento horizontalmente por uma forma de colocação.</span><span class="sxs-lookup"><span data-stu-id="4ca68-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ca68-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca68-111">Remarks</span></span>

<span data-ttu-id="4ca68-112">Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="4ca68-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="4ca68-113">Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="4ca68-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="4ca68-114">Para obter uma referência para a célula ShapePermeableX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="4ca68-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ca68-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4ca68-115">Cell name:</span></span>  <br/> |<span data-ttu-id="4ca68-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="4ca68-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="4ca68-117">Para obter uma referência para a célula ShapePermeableX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4ca68-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ca68-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4ca68-118">Section index:</span></span>  <br/> |<span data-ttu-id="4ca68-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4ca68-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4ca68-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4ca68-120">Row index:</span></span>  <br/> |<span data-ttu-id="4ca68-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="4ca68-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="4ca68-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4ca68-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4ca68-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="4ca68-123">**visSLOPermX**</span></span> <br/> |
   

