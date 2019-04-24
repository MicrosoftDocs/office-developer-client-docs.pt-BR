---
title: Célula KeepTextFlat (seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica se o texto da forma ignorará a rotação da forma em 3D. Não se aplica à rotação 2D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360435"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="4f6a6-104">Célula KeepTextFlat (seção 3-D Rotation Properties)</span><span class="sxs-lookup"><span data-stu-id="4f6a6-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="4f6a6-105">Indica se o texto da forma ignorará a rotação da forma em 3D.</span><span class="sxs-lookup"><span data-stu-id="4f6a6-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="4f6a6-106">Não se aplica à rotação 2D.</span><span class="sxs-lookup"><span data-stu-id="4f6a6-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="4f6a6-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4f6a6-107">**Value**</span></span>|<span data-ttu-id="4f6a6-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4f6a6-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f6a6-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="4f6a6-109">TRUE</span></span>  <br/> |<span data-ttu-id="4f6a6-110">O texto da forma não gira com a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="4f6a6-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="4f6a6-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f6a6-111">FALSE</span></span>  <br/> |<span data-ttu-id="4f6a6-112">O texto da forma é transformado para girar com a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="4f6a6-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f6a6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f6a6-113">Remarks</span></span>

<span data-ttu-id="4f6a6-114">Para obter uma referência para a célula **KeepTextFlat** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="4f6a6-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f6a6-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4f6a6-115">Cell name:</span></span>  <br/> |<span data-ttu-id="4f6a6-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="4f6a6-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="4f6a6-117">Para obter uma referência para a célula **KeepTextFlat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4f6a6-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f6a6-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4f6a6-118">Section index:</span></span>  <br/> |<span data-ttu-id="4f6a6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4f6a6-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4f6a6-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4f6a6-120">Row index:</span></span>  <br/> |<span data-ttu-id="4f6a6-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="4f6a6-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="4f6a6-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4f6a6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4f6a6-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="4f6a6-123">**visKeepTextFlat**</span></span> <br/> |
   

