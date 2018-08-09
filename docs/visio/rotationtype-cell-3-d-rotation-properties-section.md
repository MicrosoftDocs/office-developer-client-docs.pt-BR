---
title: Célula RotationType (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina se a forma segue uma rotação paralela, rotação de uma perspectiva ou uma rotação Oblíqua, como um inteiro de 0 a 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772778"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="29bc3-103">Célula RotationType (Seção 3-D Rotation Properties)</span><span class="sxs-lookup"><span data-stu-id="29bc3-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="29bc3-104">Determina se a forma segue uma rotação paralela, rotação de uma perspectiva ou uma rotação Oblíqua, como um inteiro de 0 a 6.</span><span class="sxs-lookup"><span data-stu-id="29bc3-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="29bc3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="29bc3-105">**Value**</span></span>|<span data-ttu-id="29bc3-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29bc3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29bc3-107">0</span><span class="sxs-lookup"><span data-stu-id="29bc3-107">0</span></span>  <br/> |<span data-ttu-id="29bc3-108">A forma não tem qualquer rotação.</span><span class="sxs-lookup"><span data-stu-id="29bc3-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="29bc3-109">1</span><span class="sxs-lookup"><span data-stu-id="29bc3-109">1</span></span>  <br/> |<span data-ttu-id="29bc3-110">A forma não tiver uma rotação paralela.</span><span class="sxs-lookup"><span data-stu-id="29bc3-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="29bc3-111">2</span><span class="sxs-lookup"><span data-stu-id="29bc3-111">2</span></span>  <br/> |<span data-ttu-id="29bc3-112">A forma não tiver uma rotação perspectiva.</span><span class="sxs-lookup"><span data-stu-id="29bc3-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="29bc3-113">3</span><span class="sxs-lookup"><span data-stu-id="29bc3-113">3</span></span>  <br/> |<span data-ttu-id="29bc3-114">A forma não tiver uma rotação de oblíqua superior à esquerda.</span><span class="sxs-lookup"><span data-stu-id="29bc3-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="29bc3-115">4</span><span class="sxs-lookup"><span data-stu-id="29bc3-115">4</span></span>  <br/> |<span data-ttu-id="29bc3-116">A forma não tiver uma rotação oblíqua à direita superior.</span><span class="sxs-lookup"><span data-stu-id="29bc3-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="29bc3-117">5</span><span class="sxs-lookup"><span data-stu-id="29bc3-117">5</span></span>  <br/> |<span data-ttu-id="29bc3-118">A forma não tiver uma rotação de oblíqua inferior à esquerda.</span><span class="sxs-lookup"><span data-stu-id="29bc3-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="29bc3-119">6</span><span class="sxs-lookup"><span data-stu-id="29bc3-119">6</span></span>  <br/> |<span data-ttu-id="29bc3-120">A forma não tiver uma parte inferior direita oblíqua rotação.</span><span class="sxs-lookup"><span data-stu-id="29bc3-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29bc3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="29bc3-121">Remarks</span></span>

<span data-ttu-id="29bc3-122">Para fazer referência à célula **RotationType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="29bc3-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29bc3-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="29bc3-123">Cell name:</span></span>  <br/> |<span data-ttu-id="29bc3-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="29bc3-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="29bc3-125">Para obter uma referência à célula **RotationType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="29bc3-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29bc3-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="29bc3-126">Section index:</span></span>  <br/> |<span data-ttu-id="29bc3-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29bc3-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="29bc3-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="29bc3-128">Row index:</span></span>  <br/> |<span data-ttu-id="29bc3-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="29bc3-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="29bc3-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="29bc3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="29bc3-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="29bc3-131">**visRotationType**</span></span> <br/> |
   

