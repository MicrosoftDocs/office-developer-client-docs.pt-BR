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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434043"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="4f4a2-103">Célula LockMoveY (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="4f4a2-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="4f4a2-104">Protege a posição vertical da forma para que ela não se mova verticalmente.</span><span class="sxs-lookup"><span data-stu-id="4f4a2-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="4f4a2-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4f4a2-105">**Value**</span></span>|<span data-ttu-id="4f4a2-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4f4a2-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4f4a2-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="4f4a2-107">TRUE</span></span>  <br/> | <span data-ttu-id="4f4a2-108">A posição vertical está protegida.</span><span class="sxs-lookup"><span data-stu-id="4f4a2-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="4f4a2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f4a2-109">FALSE</span></span>  <br/> | <span data-ttu-id="4f4a2-110">A posição vertical não está protegida.</span><span class="sxs-lookup"><span data-stu-id="4f4a2-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f4a2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f4a2-111">Remarks</span></span>

<span data-ttu-id="4f4a2-112">Para fazer referência à célula LockMoveY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4f4a2-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f4a2-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4f4a2-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4f4a2-114">LockMoveY</span><span class="sxs-lookup"><span data-stu-id="4f4a2-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="4f4a2-115">Para fazer referência à célula LockMoveY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4f4a2-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f4a2-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4f4a2-116">Section index:</span></span>  <br/> |<span data-ttu-id="4f4a2-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4f4a2-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4f4a2-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="4f4a2-118">Row index:</span></span>  <br/> |<span data-ttu-id="4f4a2-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4f4a2-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="4f4a2-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4f4a2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4f4a2-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="4f4a2-121">**visLockMoveY**</span></span> <br/> |
   

