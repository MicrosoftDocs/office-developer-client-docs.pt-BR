---
title: Célula NoShow (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indica se um caminho será exibido na página de desenho.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341080"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="feb3b-103">Célula NoShow (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="feb3b-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="feb3b-104">Indica se um caminho será exibido na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="feb3b-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="feb3b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="feb3b-105">**Value**</span></span>|<span data-ttu-id="feb3b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feb3b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="feb3b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="feb3b-107">TRUE</span></span>  <br/> | <span data-ttu-id="feb3b-108">O traço e o preenchimento do caminho representados pela seção estão ocultos.</span><span class="sxs-lookup"><span data-stu-id="feb3b-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="feb3b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="feb3b-109">FALSE</span></span>  <br/> | <span data-ttu-id="feb3b-110">O traço e o preenchimento do caminho são exibidos.</span><span class="sxs-lookup"><span data-stu-id="feb3b-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feb3b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="feb3b-111">Remarks</span></span>

<span data-ttu-id="feb3b-112">Para fazer referência à célula NoShow pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="feb3b-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="feb3b-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="feb3b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="feb3b-114">Geometry *i* . NoShow onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="feb3b-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="feb3b-115">Para fazer referência à célula NoShow pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="feb3b-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="feb3b-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="feb3b-116">Section index:</span></span>  <br/> |<span data-ttu-id="feb3b-117">**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="feb3b-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="feb3b-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="feb3b-118">Row index:</span></span>  <br/> |<span data-ttu-id="feb3b-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="feb3b-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="feb3b-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="feb3b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="feb3b-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="feb3b-121">**visCompNoShow**</span></span> <br/> |
   

