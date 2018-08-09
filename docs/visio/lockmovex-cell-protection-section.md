---
title: Célula LockMoveX (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Protege a posição horizontal da forma para que ela não se mova horizontalmente.
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772269"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="7c990-103">Célula LockMoveX (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="7c990-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="7c990-104">Protege a posição horizontal da forma para que ela não se mova horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="7c990-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="7c990-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7c990-105">**Value**</span></span>|<span data-ttu-id="7c990-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c990-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7c990-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="7c990-107">TRUE</span></span>  <br/> | <span data-ttu-id="7c990-108">A posição horizontal está protegida.</span><span class="sxs-lookup"><span data-stu-id="7c990-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="7c990-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="7c990-109">FALSE</span></span>  <br/> | <span data-ttu-id="7c990-110">A posição horizontal não está protegida.</span><span class="sxs-lookup"><span data-stu-id="7c990-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c990-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c990-111">Remarks</span></span>

<span data-ttu-id="7c990-112">Para fazer referência à célula LockMoveX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7c990-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c990-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7c990-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7c990-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="7c990-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="7c990-115">Para fazer referência à célula LockMoveX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7c990-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7c990-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7c990-116">Section index:</span></span>  <br/> |<span data-ttu-id="7c990-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7c990-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7c990-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7c990-118">Row index:</span></span>  <br/> |<span data-ttu-id="7c990-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="7c990-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="7c990-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7c990-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7c990-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="7c990-121">**visLockMoveX**</span></span> <br/> |
   

