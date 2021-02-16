---
title: Célula SketchAmount (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina a quantidade de distorção para um efeito de esboço, como um número inteiro entre 0 e 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404418"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="76e45-103">Célula SketchAmount (Seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="76e45-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="76e45-104">Determina a quantidade de distorção para um efeito de esboço, como um número inteiro entre 0 e 25.</span><span class="sxs-lookup"><span data-stu-id="76e45-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="76e45-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="76e45-105">**Value**</span></span>|<span data-ttu-id="76e45-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="76e45-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76e45-107">0</span><span class="sxs-lookup"><span data-stu-id="76e45-107">0</span></span>  <br/> |<span data-ttu-id="76e45-108">A forma não tem efeito de esboço aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="76e45-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="76e45-109">1-25</span><span class="sxs-lookup"><span data-stu-id="76e45-109">1-25</span></span>  <br/> |<span data-ttu-id="76e45-110">A forma tem distorção de esboço aplicada a ela, onde um valor de 1 é o mais distorção e 25 é o menor.</span><span class="sxs-lookup"><span data-stu-id="76e45-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76e45-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="76e45-111">Remarks</span></span>

<span data-ttu-id="76e45-112">Para fazer referência à célula **SketchAmount** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="76e45-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76e45-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="76e45-113">Cell name:</span></span>  <br/> | <span data-ttu-id="76e45-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="76e45-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="76e45-115">Para fazer referência à célula **SketchAmount** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="76e45-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76e45-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="76e45-116">Section index:</span></span>  <br/> |<span data-ttu-id="76e45-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="76e45-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="76e45-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="76e45-118">Row index:</span></span>  <br/> |<span data-ttu-id="76e45-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="76e45-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="76e45-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="76e45-120">Cell index:</span></span>  <br/> |<span data-ttu-id="76e45-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="76e45-121">**visSketchAmount**</span></span> <br/> |
   

