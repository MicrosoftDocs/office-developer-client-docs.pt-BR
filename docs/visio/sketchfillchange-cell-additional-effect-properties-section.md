---
title: Célula SketchFillChange (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina a quantidade de randomização do preenchimento da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula SketchFillChange for definido como 0%, a geometria delimitada do preenchimento de uma forma corresponde à geometria da forma. Se o valor for 100%, a geometria delimitada do preenchimento da forma não seguirá a geometria da forma.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408072"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="62cd4-105">Célula SketchFillChange (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="62cd4-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="62cd4-106">Determina a quantidade de randomização do preenchimento da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção.</span><span class="sxs-lookup"><span data-stu-id="62cd4-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="62cd4-107">Se o valor da célula **SketchFillChange** for definido como 0%, a geometria delimitada do preenchimento de uma forma corresponde à geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="62cd4-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="62cd4-108">Se o valor for 100%, a geometria delimitada do preenchimento da forma não seguirá a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="62cd4-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="62cd4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="62cd4-109">Remarks</span></span>

<span data-ttu-id="62cd4-110">Para melhores resultados, o intervalo ideal de valores para a célula **SketchFillChange** é entre 15% e 50%.</span><span class="sxs-lookup"><span data-stu-id="62cd4-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="62cd4-111">Um valor abaixo de 15% é perceptível; um valor maior que 50% é cada vez mais aleatório.</span><span class="sxs-lookup"><span data-stu-id="62cd4-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="62cd4-112">Para fazer referência à célula **SketchFillChange** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="62cd4-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62cd4-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="62cd4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="62cd4-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="62cd4-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="62cd4-115">Para fazer referência à célula **SketchFillChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="62cd4-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62cd4-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="62cd4-116">Section index:</span></span>  <br/> |<span data-ttu-id="62cd4-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="62cd4-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="62cd4-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="62cd4-118">Row index:</span></span>  <br/> |<span data-ttu-id="62cd4-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="62cd4-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="62cd4-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="62cd4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="62cd4-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="62cd4-121">**visSketchFillChange**</span></span> <br/> |
   

