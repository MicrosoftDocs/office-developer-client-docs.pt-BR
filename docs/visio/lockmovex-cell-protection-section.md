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
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348262"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="58378-103">Célula LockMoveX (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="58378-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="58378-104">Protege a posição horizontal da forma para que ela não se mova horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="58378-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="58378-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="58378-105">**Value**</span></span>|<span data-ttu-id="58378-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="58378-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="58378-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="58378-107">TRUE</span></span>  <br/> | <span data-ttu-id="58378-108">A posição horizontal está protegida.</span><span class="sxs-lookup"><span data-stu-id="58378-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="58378-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="58378-109">FALSE</span></span>  <br/> | <span data-ttu-id="58378-110">A posição horizontal não está protegida.</span><span class="sxs-lookup"><span data-stu-id="58378-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58378-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="58378-111">Remarks</span></span>

<span data-ttu-id="58378-112">Para fazer referência à célula LockMoveX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="58378-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58378-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="58378-113">Cell name:</span></span>  <br/> | <span data-ttu-id="58378-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="58378-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="58378-115">Para fazer referência à célula LockMoveX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="58378-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58378-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="58378-116">Section index:</span></span>  <br/> |<span data-ttu-id="58378-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58378-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="58378-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="58378-118">Row index:</span></span>  <br/> |<span data-ttu-id="58378-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="58378-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="58378-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="58378-120">Cell index:</span></span>  <br/> |<span data-ttu-id="58378-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="58378-121">**visLockMoveX**</span></span> <br/> |
   

