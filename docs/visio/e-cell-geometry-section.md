---
title: Célula E (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contém uma fórmula de B-spline racional não-uniforme (NURBS).
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423563"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="56b1f-103">Célula E (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="56b1f-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="56b1f-104">Contém uma fórmula de B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="56b1f-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56b1f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="56b1f-105">Remarks</span></span>

<span data-ttu-id="56b1f-106">Para fazer referência à célula E pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="56b1f-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56b1f-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="56b1f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="56b1f-108">Geometry *i* . E *j* onde *i* e *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="56b1f-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="56b1f-109">Para fazer referência à célula E pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="56b1f-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56b1f-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="56b1f-110">Section index:</span></span>  <br/> |<span data-ttu-id="56b1f-111">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56b1f-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56b1f-112">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="56b1f-112">Row index:</span></span>  <br/> |<span data-ttu-id="56b1f-113">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56b1f-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56b1f-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="56b1f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="56b1f-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="56b1f-115">**visNURBSData**</span></span> <br/> |
   

