---
title: Célula SketchLineChange (seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina a quantidade de randomização da linha da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula SketchLineChange for definido como 0%, a geometria da linha da forma corresponderá à geometria da forma. Se o valor for 100%, a geometria da linha da forma não seguirá a geometria da forma.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419503"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="cceef-105">Célula SketchLineChange (seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="cceef-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="cceef-106">Determina a quantidade de randomização da linha da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção.</span><span class="sxs-lookup"><span data-stu-id="cceef-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="cceef-107">Se o valor da célula **SketchLineChange** for definido como 0%, a geometria da linha da forma corresponderá à geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="cceef-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="cceef-108">Se o valor for 100%, a geometria da linha da forma não seguirá a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="cceef-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cceef-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="cceef-109">Remarks</span></span>

<span data-ttu-id="cceef-110">Para obter melhores resultados, o intervalo ideal de valores para a célula **SketchLineChange** está entre 15% e 50%.</span><span class="sxs-lookup"><span data-stu-id="cceef-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="cceef-111">Um valor abaixo de 15% é mal perceptível; um valor maior do que 50% pode tornar a linha excessiva demais.</span><span class="sxs-lookup"><span data-stu-id="cceef-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="cceef-112">Para obter uma referência para a célula **SketchLineChange** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cceef-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cceef-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cceef-113">Cell name:</span></span>  <br/> | <span data-ttu-id="cceef-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="cceef-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="cceef-115">Para obter uma referência para a célula **SketchLineChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cceef-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cceef-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cceef-116">Section index:</span></span>  <br/> |<span data-ttu-id="cceef-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cceef-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cceef-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cceef-118">Row index:</span></span>  <br/> |<span data-ttu-id="cceef-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="cceef-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="cceef-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cceef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cceef-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="cceef-121">**visSketchLineChange**</span></span> <br/> |
   

