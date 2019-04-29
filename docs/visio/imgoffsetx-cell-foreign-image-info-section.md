---
title: Célula ImgOffsetX (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: Determina a distância de deslocamento horizontal do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta Cortar irá alterar esse valor.
ms.openlocfilehash: d9b3e97a07bc1cadc0276905c4199861ab0590ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405230"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a><span data-ttu-id="477c9-105">Célula ImgOffsetX (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="477c9-105">ImgOffsetX Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="477c9-p102">Determina a distância de deslocamento horizontal do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta **Cortar** irá alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="477c9-p102">Determines the distance the object is offset horizontally from the origin of the object's border. The default is 0. Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="477c9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="477c9-109">Remarks</span></span>

<span data-ttu-id="477c9-110">Para fazer referência à célula ImgOffsetX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="477c9-110">To get a reference to the ImgOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="477c9-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="477c9-111">Cell name:</span></span>  <br/> | <span data-ttu-id="477c9-112">ImgOffsetX</span><span class="sxs-lookup"><span data-stu-id="477c9-112">ImgOffsetX</span></span>  <br/> |
   
<span data-ttu-id="477c9-113">Para fazer referência à célula ImgOffsetX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="477c9-113">To get a reference to the ImgOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="477c9-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="477c9-114">Section index:</span></span>  <br/> |<span data-ttu-id="477c9-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="477c9-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="477c9-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="477c9-116">Row index:</span></span>  <br/> |<span data-ttu-id="477c9-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="477c9-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="477c9-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="477c9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="477c9-119">**visFrgnImgOffsetX**</span><span class="sxs-lookup"><span data-stu-id="477c9-119">**visFrgnImgOffsetX**</span></span> <br/> |
   

