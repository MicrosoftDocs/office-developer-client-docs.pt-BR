---
title: Célula ReplaceCopyCells (seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica uma lista de células no ShapeSheet que são copiadas de uma forma antiga para a forma de substituição durante uma operação de substituição de forma.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409339"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="b4300-103">Célula ReplaceCopyCells (seção Change Shape Behavior)</span><span class="sxs-lookup"><span data-stu-id="b4300-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="b4300-104">Indica uma lista de células no ShapeSheet que são copiadas de uma forma antiga para a forma de substituição durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="b4300-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b4300-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4300-105">Remarks</span></span>

<span data-ttu-id="b4300-106">A forma mestre da substituição deve conter uma chamada de função de **dependência** na célula **ReplaceCopyCells** , onde cada argumento na função é uma referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="b4300-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="b4300-107">Essas células são copiadas da forma antiga para a forma que resulta de uma operação de substituição de forma, independentemente de onde elas estão no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="b4300-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="b4300-108">Os valores e/ou fórmulas que fazem referência a outras células são copiados para a forma resultante.</span><span class="sxs-lookup"><span data-stu-id="b4300-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="b4300-109">Se a forma resultante não tiver a célula referenciada, a célula copiada conterá apenas o valor.</span><span class="sxs-lookup"><span data-stu-id="b4300-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="b4300-110">Referências na proteção de substituição de célula **ReplaceCopyCells** definidas nas células, conforme definido na seção **proteção** e nas células **ReplaceLockFormat**, **ReplaceLockShapeData**e **ReplaceLockText** .</span><span class="sxs-lookup"><span data-stu-id="b4300-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="b4300-111">Para obter uma referência para a célula **ReplaceCopyCells** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b4300-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4300-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b4300-112">Cell name:</span></span>  <br/> | <span data-ttu-id="b4300-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="b4300-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="b4300-114">Para obter uma referência para a célula **ReplaceCopyCells** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b4300-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4300-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b4300-115">Section index:</span></span>  <br/> |<span data-ttu-id="b4300-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b4300-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b4300-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b4300-117">Row index:</span></span>  <br/> |<span data-ttu-id="b4300-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="b4300-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="b4300-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b4300-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b4300-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="b4300-120">**visReplaceCopyCells**</span></span> <br/> |
   

