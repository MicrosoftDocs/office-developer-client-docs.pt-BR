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
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771948"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="eb4bc-104">Célula Gamma (Seção Image Properties)</span><span class="sxs-lookup"><span data-stu-id="eb4bc-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="eb4bc-p102">Ajusta ou corrige a intensidade de uma imagem para um determinado dispositivo de saída, como um monitor ou scanner. O valor padrão é 1 (sem correção).</span><span class="sxs-lookup"><span data-stu-id="eb4bc-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb4bc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb4bc-107">Remarks</span></span>

<span data-ttu-id="eb4bc-108">Para fazer referência à célula Gamma pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="eb4bc-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb4bc-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="eb4bc-109">Cell name:</span></span>  <br/> | <span data-ttu-id="eb4bc-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="eb4bc-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="eb4bc-111">Para fazer referência à célula Gamma pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="eb4bc-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb4bc-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="eb4bc-112">Section index:</span></span>  <br/> |<span data-ttu-id="eb4bc-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb4bc-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb4bc-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="eb4bc-114">Row index:</span></span>  <br/> |<span data-ttu-id="eb4bc-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="eb4bc-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="eb4bc-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="eb4bc-116">Cell index:</span></span>  <br/> |<span data-ttu-id="eb4bc-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="eb4bc-117">**visImageGamma**</span></span> <br/> |
   

