---
title: Célula ImgOffsetY (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: Determina a distância de deslocamento vertical do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta Cortar irá alterar esse valor.
ms.openlocfilehash: 2930aa092a2b776ceb0c9c4677f7e5da7f5dcdda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772058"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a><span data-ttu-id="de07d-105">Célula ImgOffsetY (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="de07d-105">ImgOffsetY Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="de07d-p102">Determina a distância de deslocamento vertical do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta **Cortar** irá alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="de07d-p102">Determines the distance the object is offset vertically from the origin of the object's border. The default is 0. Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de07d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="de07d-109">Remarks</span></span>

<span data-ttu-id="de07d-110">Para fazer referência à célula ImgOffsetY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="de07d-110">To get a reference to the ImgOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de07d-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="de07d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="de07d-112">ImgOffsetY</span><span class="sxs-lookup"><span data-stu-id="de07d-112">ImgOffsetY</span></span>  <br/> |
   
<span data-ttu-id="de07d-113">Para fazer referência à célula ImgOffsetY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="de07d-113">To get a reference to the ImgOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de07d-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="de07d-114">Section index:</span></span>  <br/> |<span data-ttu-id="de07d-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="de07d-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="de07d-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="de07d-116">Row index:</span></span>  <br/> |<span data-ttu-id="de07d-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="de07d-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="de07d-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="de07d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="de07d-119">**visFrgnImgOffsetY**</span><span class="sxs-lookup"><span data-stu-id="de07d-119">**visFrgnImgOffsetY**</span></span> <br/> |
   

