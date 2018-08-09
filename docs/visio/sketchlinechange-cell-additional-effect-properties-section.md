---
title: Célula SketchLineChange (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina a quantidade de randomização da linha da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção. Se o valor da célula SketchLineChange é definido como 0%, a geometria de linha da forma faz a correspondência de geometria da forma. Se o valor é 100%, a geometria de linha da forma não seguem a geometria da forma.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772997"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="d5b23-105">Célula SketchLineChange (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="d5b23-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="d5b23-106">Determina a quantidade de randomização da linha da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção.</span><span class="sxs-lookup"><span data-stu-id="d5b23-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="d5b23-107">Se o valor da célula **SketchLineChange** é definido como 0%, a geometria de linha da forma faz a correspondência de geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="d5b23-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="d5b23-108">Se o valor é 100%, a geometria de linha da forma não seguem a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="d5b23-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d5b23-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5b23-109">Remarks</span></span>

<span data-ttu-id="d5b23-110">Para obter melhores resultados, o intervalo de valores para a célula **SketchLineChange** ideal está entre 15% e 50%.</span><span class="sxs-lookup"><span data-stu-id="d5b23-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="d5b23-111">Um valor abaixo de 15% é quase não perceptível; um valor maior do que 50% pôde tornar aleatório a linha muito grande.</span><span class="sxs-lookup"><span data-stu-id="d5b23-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="d5b23-112">Para fazer referência à célula **SketchLineChange** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d5b23-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5b23-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d5b23-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d5b23-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="d5b23-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="d5b23-115">Para obter uma referência à célula **SketchLineChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d5b23-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5b23-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d5b23-116">Section index:</span></span>  <br/> |<span data-ttu-id="d5b23-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d5b23-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d5b23-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d5b23-118">Row index:</span></span>  <br/> |<span data-ttu-id="d5b23-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="d5b23-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="d5b23-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d5b23-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d5b23-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="d5b23-121">**visSketchLineChange**</span></span> <br/> |
   

