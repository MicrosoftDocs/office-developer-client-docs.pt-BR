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
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771787"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="52203-103">Célula E (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="52203-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="52203-104">Contém uma fórmula de B-spline racional não-uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="52203-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52203-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="52203-105">Remarks</span></span>

<span data-ttu-id="52203-106">Para fazer referência à célula E pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="52203-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52203-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="52203-107">Cell name:</span></span>  <br/> | <span data-ttu-id="52203-108">Geometria *i* . F *j* onde *i* e *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="52203-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="52203-109">Para fazer referência à célula E pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="52203-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52203-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="52203-110">Section index:</span></span>  <br/> |<span data-ttu-id="52203-111">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="52203-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="52203-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="52203-112">Row index:</span></span>  <br/> |<span data-ttu-id="52203-113">**visRowVertex** +  *j* onde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="52203-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="52203-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="52203-114">Cell index:</span></span>  <br/> |<span data-ttu-id="52203-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="52203-115">**visNURBSData**</span></span> <br/> |
   

