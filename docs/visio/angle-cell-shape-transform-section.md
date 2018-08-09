---
title: Célula Angle (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Representa o ângulo de rotação atual da forma em relação ao pai. A fórmula padrão para determinar o ângulo de rotação de uma forma 1D é: =ATAN2(EndY-BeginY,EndX-BeginX).'
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771260"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="f3a58-104">Célula Angle (Seção Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="f3a58-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="f3a58-p102">Representa o ângulo de rotação atual da forma em relação ao pai. A fórmula padrão para determinar o ângulo de rotação de uma forma 1D é: =ATAN2(EndY-BeginY,EndX-BeginX).</span><span class="sxs-lookup"><span data-stu-id="f3a58-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3a58-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3a58-107">Remarks</span></span>

<span data-ttu-id="f3a58-108">Para fazer referência à célula Angle pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f3a58-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3a58-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f3a58-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f3a58-110">Angle</span><span class="sxs-lookup"><span data-stu-id="f3a58-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="f3a58-111">Para fazer referência à célula Angle pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f3a58-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3a58-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f3a58-112">Section index:</span></span>  <br/> |<span data-ttu-id="f3a58-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3a58-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f3a58-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f3a58-114">Row index:</span></span>  <br/> |<span data-ttu-id="f3a58-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="f3a58-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="f3a58-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f3a58-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f3a58-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="f3a58-117">**visXFormAngle**</span></span> <br/> |
   

