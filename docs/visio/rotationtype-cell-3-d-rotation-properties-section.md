---
title: Célula RotationType (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422940"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="bb164-103">Célula RotationType (Seção 3-D Rotation Properties)</span><span class="sxs-lookup"><span data-stu-id="bb164-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="bb164-104">Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6.</span><span class="sxs-lookup"><span data-stu-id="bb164-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="bb164-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bb164-105">**Value**</span></span>|<span data-ttu-id="bb164-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bb164-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb164-107">0</span><span class="sxs-lookup"><span data-stu-id="bb164-107">0</span></span>  <br/> |<span data-ttu-id="bb164-108">A forma não tem rotação.</span><span class="sxs-lookup"><span data-stu-id="bb164-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="bb164-109">1 </span><span class="sxs-lookup"><span data-stu-id="bb164-109">1</span></span>  <br/> |<span data-ttu-id="bb164-110">A forma tem uma rotação paralela.</span><span class="sxs-lookup"><span data-stu-id="bb164-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="bb164-111">2 </span><span class="sxs-lookup"><span data-stu-id="bb164-111">2</span></span>  <br/> |<span data-ttu-id="bb164-112">A forma tem uma rotação de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="bb164-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="bb164-113">3 </span><span class="sxs-lookup"><span data-stu-id="bb164-113">3</span></span>  <br/> |<span data-ttu-id="bb164-114">A forma tem uma rotação oblíqua superior esquerda.</span><span class="sxs-lookup"><span data-stu-id="bb164-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="bb164-115">4 </span><span class="sxs-lookup"><span data-stu-id="bb164-115">4</span></span>  <br/> |<span data-ttu-id="bb164-116">A forma tem uma rotação oblíqua superior direita.</span><span class="sxs-lookup"><span data-stu-id="bb164-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="bb164-117">5 </span><span class="sxs-lookup"><span data-stu-id="bb164-117">5</span></span>  <br/> |<span data-ttu-id="bb164-118">A forma tem uma rotação oblíqua inferior esquerda.</span><span class="sxs-lookup"><span data-stu-id="bb164-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="bb164-119">6 </span><span class="sxs-lookup"><span data-stu-id="bb164-119">6</span></span>  <br/> |<span data-ttu-id="bb164-120">A forma tem uma rotação oblíqua direita inferior.</span><span class="sxs-lookup"><span data-stu-id="bb164-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb164-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb164-121">Remarks</span></span>

<span data-ttu-id="bb164-122">Para fazer referência à célula **RotationType** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="bb164-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb164-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bb164-123">Cell name:</span></span>  <br/> |<span data-ttu-id="bb164-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="bb164-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="bb164-125">Para fazer referência à célula **RotationType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bb164-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb164-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bb164-126">Section index:</span></span>  <br/> |<span data-ttu-id="bb164-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bb164-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bb164-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="bb164-128">Row index:</span></span>  <br/> |<span data-ttu-id="bb164-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="bb164-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="bb164-130">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="bb164-130">Cell index:</span></span>  <br/> |<span data-ttu-id="bb164-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="bb164-131">**visRotationType**</span></span> <br/> |
   

