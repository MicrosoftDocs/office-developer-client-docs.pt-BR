---
title: Célula Rotationtype (seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315670"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="ae102-103">Célula Rotationtype (seção 3-D Rotation Properties)</span><span class="sxs-lookup"><span data-stu-id="ae102-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="ae102-104">Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6.</span><span class="sxs-lookup"><span data-stu-id="ae102-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="ae102-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae102-105">**Value**</span></span>|<span data-ttu-id="ae102-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae102-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae102-107">,0</span><span class="sxs-lookup"><span data-stu-id="ae102-107">0</span></span>  <br/> |<span data-ttu-id="ae102-108">A forma não tem nenhuma rotação.</span><span class="sxs-lookup"><span data-stu-id="ae102-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="ae102-109">1</span><span class="sxs-lookup"><span data-stu-id="ae102-109">1</span></span>  <br/> |<span data-ttu-id="ae102-110">A forma tem uma rotação paralela.</span><span class="sxs-lookup"><span data-stu-id="ae102-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="ae102-111">duas</span><span class="sxs-lookup"><span data-stu-id="ae102-111">2</span></span>  <br/> |<span data-ttu-id="ae102-112">A forma tem uma rotação em perspectiva.</span><span class="sxs-lookup"><span data-stu-id="ae102-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="ae102-113">3D</span><span class="sxs-lookup"><span data-stu-id="ae102-113">3</span></span>  <br/> |<span data-ttu-id="ae102-114">A forma tem uma rotação oblíquo superior esquerda.</span><span class="sxs-lookup"><span data-stu-id="ae102-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="ae102-115">quatro</span><span class="sxs-lookup"><span data-stu-id="ae102-115">4</span></span>  <br/> |<span data-ttu-id="ae102-116">A forma tem uma rotação oblíqua para a direita superior.</span><span class="sxs-lookup"><span data-stu-id="ae102-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="ae102-117">0,5</span><span class="sxs-lookup"><span data-stu-id="ae102-117">5</span></span>  <br/> |<span data-ttu-id="ae102-118">A forma tem uma rotação oblíquo inferior à esquerda.</span><span class="sxs-lookup"><span data-stu-id="ae102-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="ae102-119">6</span><span class="sxs-lookup"><span data-stu-id="ae102-119">6</span></span>  <br/> |<span data-ttu-id="ae102-120">A forma tem uma rotação oblíqua inferior à direita.</span><span class="sxs-lookup"><span data-stu-id="ae102-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae102-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae102-121">Remarks</span></span>

<span data-ttu-id="ae102-122">Para obter uma referência para a \*\*\*\* célula rotationtype pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="ae102-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae102-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ae102-123">Cell name:</span></span>  <br/> |<span data-ttu-id="ae102-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="ae102-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="ae102-125">Para obter uma referência para a \*\*\*\* célula rotationtype pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ae102-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae102-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ae102-126">Section index:</span></span>  <br/> |<span data-ttu-id="ae102-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae102-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ae102-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ae102-128">Row index:</span></span>  <br/> |<span data-ttu-id="ae102-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="ae102-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="ae102-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ae102-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ae102-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="ae102-131">**visRotationType**</span></span> <br/> |
   

