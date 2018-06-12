---
title: Célula ReplaceCopyCells (seção de comportamento de forma alterar)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica uma lista das células na ShapeSheet que são copiadas de uma forma antiga à forma de substituição durante uma operação de substituição de forma.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772681"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="58951-103">Célula ReplaceCopyCells (seção de comportamento de forma alterar)</span><span class="sxs-lookup"><span data-stu-id="58951-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="58951-104">Indica uma lista das células na ShapeSheet que são copiadas de uma forma antiga à forma de substituição durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="58951-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="58951-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="58951-105">Remarks</span></span>

<span data-ttu-id="58951-106">A forma mestra da substituição deve conter uma chamada de função **DEPENDSON** na célula **ReplaceCopyCells** , onde cada argumento na função for uma referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="58951-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="58951-107">Essas células são copiadas da forma antiga à forma resultante de uma operação de substituição de forma, independentemente de onde eles estão localizados no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="58951-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="58951-108">Valores e/ou em fórmulas que fazem referência a outras células são copiadas para a forma resultante.</span><span class="sxs-lookup"><span data-stu-id="58951-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="58951-109">Se a forma resultante não tiver a célula referenciada, a célula copiada contém somente o valor.</span><span class="sxs-lookup"><span data-stu-id="58951-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="58951-110">Referências na célula **ReplaceCopyCells** substituem o conjunto de proteção em células, conforme definido na seção de **proteção** e a **ReplaceLockFormat**, **ReplaceLockShapeData**e **ReplaceLockText** células.</span><span class="sxs-lookup"><span data-stu-id="58951-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="58951-111">Para fazer referência à célula **ReplaceCopyCells** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="58951-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58951-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="58951-112">Cell name:</span></span>  <br/> | <span data-ttu-id="58951-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="58951-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="58951-114">Para obter uma referência à célula **ReplaceCopyCells** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="58951-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58951-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="58951-115">Section index:</span></span>  <br/> |<span data-ttu-id="58951-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58951-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="58951-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="58951-117">Row index:</span></span>  <br/> |<span data-ttu-id="58951-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="58951-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="58951-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="58951-119">Cell index:</span></span>  <br/> |<span data-ttu-id="58951-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="58951-120">**visReplaceCopyCells**</span></span> <br/> |
   

