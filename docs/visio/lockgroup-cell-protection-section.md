---
title: Célula LockGroup (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Protege um grupo impedindo-o de ser desagrupado.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341789"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="e6bc7-103">Célula LockGroup (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="e6bc7-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="e6bc7-104">Protege um grupo impedindo-o de ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="e6bc7-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="e6bc7-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e6bc7-105">**Value**</span></span>|<span data-ttu-id="e6bc7-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e6bc7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6bc7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e6bc7-107">TRUE</span></span>  <br/> |<span data-ttu-id="e6bc7-108">O grupo não pode ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="e6bc7-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="e6bc7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e6bc7-109">FALSE</span></span>  <br/> |<span data-ttu-id="e6bc7-110">O grupo pode ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="e6bc7-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6bc7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6bc7-111">Remarks</span></span>

<span data-ttu-id="e6bc7-112">A definição do valor LockGroupCell como TRUE também impede a exclusão de formas que sejam membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="e6bc7-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="e6bc7-113">Para obter uma referência para a célula LockGroup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e6bc7-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6bc7-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e6bc7-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e6bc7-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="e6bc7-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="e6bc7-116">Para obter uma referência para a célula LockGroup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e6bc7-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6bc7-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e6bc7-117">Section index:</span></span>  <br/> |<span data-ttu-id="e6bc7-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e6bc7-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e6bc7-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e6bc7-119">Row index:</span></span>  <br/> |<span data-ttu-id="e6bc7-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e6bc7-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="e6bc7-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e6bc7-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e6bc7-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="e6bc7-122">**visLockGroup**</span></span> <br/> |
   

