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
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772246"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="cb9a7-103">Célula LockEnd (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="cb9a7-104">Protege o ponto de extremidade (EndX, EndY) de uma forma 1D para uma localização específica.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="cb9a7-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-105">**Value**</span></span>|<span data-ttu-id="cb9a7-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cb9a7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="cb9a7-107">TRUE</span></span>  <br/> | <span data-ttu-id="cb9a7-108">O ponto de extremidade está protegido.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="cb9a7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb9a7-109">FALSE</span></span>  <br/> | <span data-ttu-id="cb9a7-110">O ponto de extremidade não está protegido.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb9a7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb9a7-111">Remarks</span></span>

<span data-ttu-id="cb9a7-112">Para fazer referência à célula LockEnd pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb9a7-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="cb9a7-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="cb9a7-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="cb9a7-115">Para fazer referência à célula LockEnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb9a7-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-116">Section index:</span></span>  <br/> |<span data-ttu-id="cb9a7-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cb9a7-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-118">Row index:</span></span>  <br/> |<span data-ttu-id="cb9a7-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="cb9a7-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cb9a7-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-121">**visLockEnd**</span></span> <br/> |
   

