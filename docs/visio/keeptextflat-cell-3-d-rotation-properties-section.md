---
title: Célula KeepTextFlat Cell (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica se o texto de uma forma irá ignorar a rotação da forma em 3D. Não se aplicam a rotação 2D.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772136"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="b6261-104">Célula KeepTextFlat Cell (Seção 3-D Rotation Properties)</span><span class="sxs-lookup"><span data-stu-id="b6261-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="b6261-105">Indica se o texto de uma forma irá ignorar a rotação da forma em 3D.</span><span class="sxs-lookup"><span data-stu-id="b6261-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="b6261-106">Não se aplicam a rotação 2D.</span><span class="sxs-lookup"><span data-stu-id="b6261-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="b6261-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b6261-107">**Value**</span></span>|<span data-ttu-id="b6261-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b6261-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6261-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="b6261-109">TRUE</span></span>  <br/> |<span data-ttu-id="b6261-110">Texto da forma não gira com a geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="b6261-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="b6261-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="b6261-111">FALSE</span></span>  <br/> |<span data-ttu-id="b6261-112">Texto da forma é transformado para girar com geometria da forma.</span><span class="sxs-lookup"><span data-stu-id="b6261-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6261-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6261-113">Remarks</span></span>

<span data-ttu-id="b6261-114">Para fazer referência à célula **KeepTextFlat** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b6261-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6261-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b6261-115">Cell name:</span></span>  <br/> |<span data-ttu-id="b6261-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="b6261-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="b6261-117">Para obter uma referência à célula **KeepTextFlat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b6261-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6261-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b6261-118">Section index:</span></span>  <br/> |<span data-ttu-id="b6261-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6261-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b6261-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b6261-120">Row index:</span></span>  <br/> |<span data-ttu-id="b6261-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="b6261-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="b6261-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b6261-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b6261-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="b6261-123">**visKeepTextFlat**</span></span> <br/> |
   

