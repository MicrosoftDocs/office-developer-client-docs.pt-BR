---
title: Célula Sharpen (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Ajusta a nitidez de uma imagem de bitmap. O valor padrão é 0%. Ajustar a nitidez focaliza uma imagem aumentando o contraste dos pixels adjacentes.
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415919"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="a6795-105">Célula Sharpen (Seção Image Properties)</span><span class="sxs-lookup"><span data-stu-id="a6795-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="a6795-106">Ajusta a nitidez de uma imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="a6795-106">Sharpens a bitmap image.</span></span> <span data-ttu-id="a6795-107">O valor padrão é 0%.</span><span class="sxs-lookup"><span data-stu-id="a6795-107">The default value is 0%.</span></span> <span data-ttu-id="a6795-108">Ajustar a nitidez focaliza uma imagem aumentando o contraste dos pixels adjacentes.</span><span class="sxs-lookup"><span data-stu-id="a6795-108">Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6795-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6795-109">Remarks</span></span>

<span data-ttu-id="a6795-110">Para fazer referência à célula Sharpen pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a6795-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6795-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a6795-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a6795-112">Nitidez</span><span class="sxs-lookup"><span data-stu-id="a6795-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="a6795-113">Para fazer referência à célula Sharpen pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a6795-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6795-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a6795-114">Section index:</span></span>  <br/> |<span data-ttu-id="a6795-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6795-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a6795-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="a6795-116">Row index:</span></span>  <br/> |<span data-ttu-id="a6795-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="a6795-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="a6795-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="a6795-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a6795-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="a6795-119">**visImageSharpen**</span></span> <br/> |
   

