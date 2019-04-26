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
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360246"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="c2582-104">Célula Clareza (Seção Imagem Propriedades)</span><span class="sxs-lookup"><span data-stu-id="c2582-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="c2582-105">Remove os ruídos (pixels com níveis de cor distribuídos aleatoriamente) de uma imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="c2582-105">Removes noise (pixels with randomly distributed color levels) from a bitmap image.</span></span> <span data-ttu-id="c2582-106">O valor padrão é 0%.</span><span class="sxs-lookup"><span data-stu-id="c2582-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2582-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2582-107">Remarks</span></span>

<span data-ttu-id="c2582-108">Para fazer referência à célula Denoise pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c2582-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2582-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c2582-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c2582-110">Clareza</span><span class="sxs-lookup"><span data-stu-id="c2582-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="c2582-111">Para fazer referência à célula Denoise pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c2582-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2582-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c2582-112">Section index:</span></span>  <br/> |<span data-ttu-id="c2582-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2582-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2582-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c2582-114">Row index:</span></span>  <br/> |<span data-ttu-id="c2582-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="c2582-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="c2582-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="c2582-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c2582-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="c2582-117">**visImageDenoise**</span></span> <br/> |
   

