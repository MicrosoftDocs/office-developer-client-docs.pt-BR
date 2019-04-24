---
title: Célula Gamma (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajusta ou corrige a intensidade de uma imagem para um determinado dispositivo de saída, como um monitor ou scanner. O valor padrão é 1 (sem correção).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315201"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="780a5-104">Célula Gamma (Seção Image Properties)</span><span class="sxs-lookup"><span data-stu-id="780a5-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="780a5-p102">Ajusta ou corrige a intensidade de uma imagem para um determinado dispositivo de saída, como um monitor ou scanner. O valor padrão é 1 (sem correção).</span><span class="sxs-lookup"><span data-stu-id="780a5-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="780a5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="780a5-107">Remarks</span></span>

<span data-ttu-id="780a5-108">Para fazer referência à célula Gamma pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="780a5-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="780a5-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="780a5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="780a5-110">Gama</span><span class="sxs-lookup"><span data-stu-id="780a5-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="780a5-111">Para fazer referência à célula Gamma pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="780a5-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="780a5-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="780a5-112">Section index:</span></span>  <br/> |<span data-ttu-id="780a5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="780a5-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="780a5-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="780a5-114">Row index:</span></span>  <br/> |<span data-ttu-id="780a5-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="780a5-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="780a5-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="780a5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="780a5-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="780a5-117">**visImageGamma**</span></span> <br/> |
   

