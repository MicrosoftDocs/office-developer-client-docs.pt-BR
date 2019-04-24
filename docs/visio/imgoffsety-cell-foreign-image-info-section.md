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
ms.openlocfilehash: 908972216a24370bc48990ddc99a36da9274d648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344734"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a><span data-ttu-id="c9603-105">Célula ImgOffsetY (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="c9603-105">ImgOffsetY Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="c9603-p102">Determina a distância de deslocamento vertical do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta **Cortar** irá alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="c9603-p102">Determines the distance the object is offset vertically from the origin of the object's border. The default is 0. Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9603-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9603-109">Remarks</span></span>

<span data-ttu-id="c9603-110">Para fazer referência à célula ImgOffsetY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c9603-110">To get a reference to the ImgOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9603-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c9603-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c9603-112">ImgOffsetY</span><span class="sxs-lookup"><span data-stu-id="c9603-112">ImgOffsetY</span></span>  <br/> |
   
<span data-ttu-id="c9603-113">Para fazer referência à célula ImgOffsetY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c9603-113">To get a reference to the ImgOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9603-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c9603-114">Section index:</span></span>  <br/> |<span data-ttu-id="c9603-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9603-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c9603-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c9603-116">Row index:</span></span>  <br/> |<span data-ttu-id="c9603-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="c9603-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="c9603-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c9603-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c9603-119">**visFrgnImgOffsetY**</span><span class="sxs-lookup"><span data-stu-id="c9603-119">**visFrgnImgOffsetY**</span></span> <br/> |
   

