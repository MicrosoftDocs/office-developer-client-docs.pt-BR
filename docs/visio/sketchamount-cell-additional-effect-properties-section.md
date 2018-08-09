---
title: Célula SketchAmount (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina a quantidade de distorção para um efeito de esboço, como um número inteiro entre 0 e 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772994"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="3915a-103">Célula SketchAmount (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="3915a-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="3915a-104">Determina a quantidade de distorção para um efeito de esboço, como um número inteiro entre 0 e 25.</span><span class="sxs-lookup"><span data-stu-id="3915a-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="3915a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3915a-105">**Value**</span></span>|<span data-ttu-id="3915a-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3915a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3915a-107">0</span><span class="sxs-lookup"><span data-stu-id="3915a-107">0</span></span>  <br/> |<span data-ttu-id="3915a-108">A forma não tem nenhum efeito de esboço aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="3915a-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="3915a-109">1-25</span><span class="sxs-lookup"><span data-stu-id="3915a-109">1-25</span></span>  <br/> |<span data-ttu-id="3915a-110">A forma não tiver aplicada a ele, onde um valor de 1 é a maioria das distorção e é de 25 de distorção de esboço a menos.</span><span class="sxs-lookup"><span data-stu-id="3915a-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3915a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3915a-111">Remarks</span></span>

<span data-ttu-id="3915a-112">Para fazer referência à célula **SketchAmount** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="3915a-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3915a-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3915a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3915a-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="3915a-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="3915a-115">Para obter uma referência à célula **SketchAmount** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3915a-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3915a-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3915a-116">Section index:</span></span>  <br/> |<span data-ttu-id="3915a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3915a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3915a-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="3915a-118">Row index:</span></span>  <br/> |<span data-ttu-id="3915a-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="3915a-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="3915a-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3915a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3915a-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="3915a-121">**visSketchAmount**</span></span> <br/> |
   

