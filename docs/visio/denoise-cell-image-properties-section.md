---
title: Célula Denoise (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Remove os ruídos (pixels com níveis de cor distribuídos aleatoriamente) de uma imagem de bitmap. O valor padrão é 0%.
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771720"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="60fba-104">Célula Denoise (Seção Image Properties)</span><span class="sxs-lookup"><span data-stu-id="60fba-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="60fba-p102">Remove os ruídos (pixels com níveis de cor distribuídos aleatoriamente) de uma imagem de bitmap. O valor padrão é 0%.</span><span class="sxs-lookup"><span data-stu-id="60fba-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60fba-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="60fba-107">Remarks</span></span>

<span data-ttu-id="60fba-108">Para fazer referência à célula Denoise pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="60fba-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60fba-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="60fba-109">Cell name:</span></span>  <br/> | <span data-ttu-id="60fba-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="60fba-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="60fba-111">Para fazer referência à célula Denoise pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="60fba-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60fba-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="60fba-112">Section index:</span></span>  <br/> |<span data-ttu-id="60fba-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="60fba-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="60fba-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="60fba-114">Row index:</span></span>  <br/> |<span data-ttu-id="60fba-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="60fba-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="60fba-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="60fba-116">Cell index:</span></span>  <br/> |<span data-ttu-id="60fba-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="60fba-117">**visImageDenoise**</span></span> <br/> |
   

