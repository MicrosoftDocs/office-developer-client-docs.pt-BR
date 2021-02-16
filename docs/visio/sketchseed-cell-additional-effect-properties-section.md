---
title: Célula SketchSeed (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Representa um valor de randomização usado para determinar a geometria de um efeito de esboço, como um inteiro positivo. O valor da célula SketchSeed é criado aleatoriamente quando um efeito de esboço é aplicado à forma.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434393"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="37fb9-104">Célula SketchSeed (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="37fb9-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="37fb9-105">Representa um valor de randomização usado para determinar a geometria de um efeito de esboço, como um inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="37fb9-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="37fb9-106">O valor da célula **SketchSeed** é criado aleatoriamente quando um efeito de esboço é aplicado à forma.</span><span class="sxs-lookup"><span data-stu-id="37fb9-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="37fb9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="37fb9-107">Remarks</span></span>

<span data-ttu-id="37fb9-108">Para fazer referência à célula **SketchSeed** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="37fb9-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37fb9-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="37fb9-109">Cell name:</span></span>  <br/> | <span data-ttu-id="37fb9-110">SketchSeed</span><span class="sxs-lookup"><span data-stu-id="37fb9-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="37fb9-111">Para fazer referência à célula **SketchSeed** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="37fb9-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37fb9-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="37fb9-112">Section index:</span></span>  <br/> |<span data-ttu-id="37fb9-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37fb9-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37fb9-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="37fb9-114">Row index:</span></span>  <br/> |<span data-ttu-id="37fb9-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="37fb9-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="37fb9-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="37fb9-116">Cell index:</span></span>  <br/> |<span data-ttu-id="37fb9-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="37fb9-117">**visSketchSeed**</span></span> <br/> |
   

