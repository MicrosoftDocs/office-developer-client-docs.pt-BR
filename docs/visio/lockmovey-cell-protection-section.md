---
title: Célula LockMoveY (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Protege a posição vertical da forma para que ela não se mova verticalmente.
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348346"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="aec2e-103">Célula LockMoveY (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="aec2e-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="aec2e-104">Protege a posição vertical da forma para que ela não se mova verticalmente.</span><span class="sxs-lookup"><span data-stu-id="aec2e-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="aec2e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="aec2e-105">**Value**</span></span>|<span data-ttu-id="aec2e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aec2e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="aec2e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="aec2e-107">TRUE</span></span>  <br/> | <span data-ttu-id="aec2e-108">A posição vertical está protegida.</span><span class="sxs-lookup"><span data-stu-id="aec2e-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="aec2e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="aec2e-109">FALSE</span></span>  <br/> | <span data-ttu-id="aec2e-110">A posição vertical não está protegida.</span><span class="sxs-lookup"><span data-stu-id="aec2e-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aec2e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="aec2e-111">Remarks</span></span>

<span data-ttu-id="aec2e-112">Para fazer referência à célula LockMoveY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="aec2e-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aec2e-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="aec2e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="aec2e-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="aec2e-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="aec2e-115">Para fazer referência à célula LockMoveY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="aec2e-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aec2e-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="aec2e-116">Section index:</span></span>  <br/> |<span data-ttu-id="aec2e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aec2e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aec2e-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="aec2e-118">Row index:</span></span>  <br/> |<span data-ttu-id="aec2e-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="aec2e-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="aec2e-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="aec2e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="aec2e-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="aec2e-121">**visLockMoveY**</span></span> <br/> |
   

