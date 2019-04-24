---
title: Célula LockAspect (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Protege a taxa de proporção da forma para que ela somente seja dimensionada proporcionalmente e não em uma dimensão única.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359637"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="503a7-103">Célula LockAspect (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="503a7-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="503a7-104">Protege a taxa de proporção da forma para que ela somente seja dimensionada proporcionalmente e não em uma dimensão única.</span><span class="sxs-lookup"><span data-stu-id="503a7-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="503a7-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="503a7-105">**Value**</span></span>|<span data-ttu-id="503a7-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="503a7-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="503a7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="503a7-107">TRUE</span></span>  <br/> | <span data-ttu-id="503a7-108">A taxa de proporção está protegida.</span><span class="sxs-lookup"><span data-stu-id="503a7-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="503a7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="503a7-109">FALSE</span></span>  <br/> | <span data-ttu-id="503a7-110">A taxa de proporção não está protegida.</span><span class="sxs-lookup"><span data-stu-id="503a7-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="503a7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="503a7-111">Remarks</span></span>

<span data-ttu-id="503a7-112">Para fazer referência à célula LockAspect pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="503a7-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="503a7-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="503a7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="503a7-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="503a7-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="503a7-115">Para fazer referência à célula LockAspect pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="503a7-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="503a7-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="503a7-116">Section index:</span></span>  <br/> |<span data-ttu-id="503a7-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="503a7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="503a7-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="503a7-118">Row index:</span></span>  <br/> |<span data-ttu-id="503a7-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="503a7-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="503a7-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="503a7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="503a7-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="503a7-121">**visLockAspect**</span></span> <br/> |
   

