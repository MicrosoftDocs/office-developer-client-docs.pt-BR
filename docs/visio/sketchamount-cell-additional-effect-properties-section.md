---
title: Célula SketchAmount (seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina a quantidade de distorção para um efeito de esboço, como um inteiro entre 0 e 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314767"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="2ca5f-103">Célula SketchAmount (seção Additional Effect Properties)</span><span class="sxs-lookup"><span data-stu-id="2ca5f-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="2ca5f-104">Determina a quantidade de distorção para um efeito de esboço, como um inteiro entre 0 e 25.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="2ca5f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2ca5f-105">**Value**</span></span>|<span data-ttu-id="2ca5f-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2ca5f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ca5f-107">,0</span><span class="sxs-lookup"><span data-stu-id="2ca5f-107">0</span></span>  <br/> |<span data-ttu-id="2ca5f-108">A forma não tem efeito de esboço aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="2ca5f-109">1-25</span><span class="sxs-lookup"><span data-stu-id="2ca5f-109">1-25</span></span>  <br/> |<span data-ttu-id="2ca5f-110">A forma tem distorção de esboço aplicada a ela, onde um valor de 1 é a maior distorção e 25 é o menos.</span><span class="sxs-lookup"><span data-stu-id="2ca5f-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ca5f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ca5f-111">Remarks</span></span>

<span data-ttu-id="2ca5f-112">Para obter uma referência para a célula **SketchAmount** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ca5f-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2ca5f-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="2ca5f-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="2ca5f-115">Para obter uma referência para a célula **SketchAmount** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ca5f-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-116">Section index:</span></span>  <br/> |<span data-ttu-id="2ca5f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2ca5f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2ca5f-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-118">Row index:</span></span>  <br/> |<span data-ttu-id="2ca5f-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="2ca5f-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="2ca5f-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2ca5f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2ca5f-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="2ca5f-121">**visSketchAmount**</span></span> <br/> |
   

