---
title: Célula SketchFillChange (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina a quantidade de randomização do preenchimento da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção. Se o valor da célula SketchFillChange é definido como 0%, a geometria de contorno de preenchimento de uma forma faz a correspondência de geometria da forma. Se o valor é 100%, a geometria de contorno de preenchimento da forma não seguem a geometria da forma.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773002"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="5e86f-105">Célula SketchFillChange (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="5e86f-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="5e86f-106">Determina a quantidade de randomização do preenchimento da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção.</span><span class="sxs-lookup"><span data-stu-id="5e86f-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="5e86f-107">Se o valor da célula **SketchFillChange** é definido como 0%, a geometria de contorno de preenchimento de uma forma faz a correspondência de geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="5e86f-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="5e86f-108">Se o valor é 100%, a geometria de contorno de preenchimento da forma não seguem a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="5e86f-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5e86f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e86f-109">Remarks</span></span>

<span data-ttu-id="5e86f-110">Para obter melhores resultados, o intervalo de valores para a célula **SketchFillChange** ideal está entre 15% e 50%.</span><span class="sxs-lookup"><span data-stu-id="5e86f-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="5e86f-111">Um valor abaixo de 15% é quase não perceptível; um valor maior do que 50% cada vez mais é aleatória.</span><span class="sxs-lookup"><span data-stu-id="5e86f-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="5e86f-112">Para fazer referência à célula **SketchFillChange** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="5e86f-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5e86f-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5e86f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5e86f-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="5e86f-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="5e86f-115">Para obter uma referência à célula **SketchFillChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5e86f-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5e86f-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5e86f-116">Section index:</span></span>  <br/> |<span data-ttu-id="5e86f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5e86f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5e86f-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5e86f-118">Row index:</span></span>  <br/> |<span data-ttu-id="5e86f-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="5e86f-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="5e86f-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5e86f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5e86f-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="5e86f-121">**visSketchFillChange**</span></span> <br/> |
   

