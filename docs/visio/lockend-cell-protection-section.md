---
title: Célula LockEnd (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Protege o ponto de extremidade (EndX, EndY) de uma forma 1D para uma localização específica.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359595"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="1227f-103">Célula LockEnd (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="1227f-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="1227f-104">Protege o ponto de extremidade (EndX, EndY) de uma forma 1D para uma localização específica.</span><span class="sxs-lookup"><span data-stu-id="1227f-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="1227f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1227f-105">**Value**</span></span>|<span data-ttu-id="1227f-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1227f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1227f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1227f-107">TRUE</span></span>  <br/> | <span data-ttu-id="1227f-108">O ponto de extremidade está protegido.</span><span class="sxs-lookup"><span data-stu-id="1227f-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="1227f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1227f-109">FALSE</span></span>  <br/> | <span data-ttu-id="1227f-110">O ponto de extremidade não está protegido.</span><span class="sxs-lookup"><span data-stu-id="1227f-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1227f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1227f-111">Remarks</span></span>

<span data-ttu-id="1227f-112">Para fazer referência à célula LockEnd pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="1227f-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1227f-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1227f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1227f-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="1227f-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="1227f-115">Para fazer referência à célula LockEnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1227f-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1227f-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1227f-116">Section index:</span></span>  <br/> |<span data-ttu-id="1227f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1227f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1227f-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1227f-118">Row index:</span></span>  <br/> |<span data-ttu-id="1227f-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="1227f-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="1227f-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1227f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1227f-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="1227f-121">**visLockEnd**</span></span> <br/> |
   

