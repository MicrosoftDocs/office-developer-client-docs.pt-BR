---
title: Célula SketchLineWeight (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Determina a espessura adicional adicionada a espessura da linha como o resultado de um efeito de esboço, em pontos de 0 a 50. A espessura da linha de uma forma aumenta à medida que o valor do SketchLineWeight célula aumenta.
ms.openlocfilehash: 9ab99faab907ddf0d944abbeea39672906b4c03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773014"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="61703-104">Célula SketchLineWeight (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="61703-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="61703-105">Determina a espessura adicional adicionada a espessura da linha como o resultado de um efeito de esboço, em pontos de 0 a 50.</span><span class="sxs-lookup"><span data-stu-id="61703-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="61703-106">A espessura da linha de uma forma aumenta à medida que o valor do **SketchLineWeight** célula aumenta.</span><span class="sxs-lookup"><span data-stu-id="61703-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61703-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="61703-107">Remarks</span></span>

<span data-ttu-id="61703-108">Para fazer referência à célula **SketchLineWeight** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="61703-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61703-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="61703-109">Cell name:</span></span>  <br/> | <span data-ttu-id="61703-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="61703-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="61703-111">Para obter uma referência à célula **SketchLineWeight** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="61703-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61703-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="61703-112">Section index:</span></span>  <br/> |<span data-ttu-id="61703-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61703-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="61703-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="61703-114">Row index:</span></span>  <br/> |<span data-ttu-id="61703-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="61703-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="61703-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="61703-116">Cell index:</span></span>  <br/> |<span data-ttu-id="61703-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="61703-117">**visSketchLineWeight**</span></span> <br/> |
   

