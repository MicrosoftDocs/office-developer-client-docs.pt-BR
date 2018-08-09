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
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772265"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="9532e-103">Célula LockGroup (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="9532e-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="9532e-104">Protege um grupo impedindo-o de ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="9532e-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="9532e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9532e-105">**Value**</span></span>|<span data-ttu-id="9532e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9532e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9532e-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="9532e-107">TRUE</span></span>  <br/> |<span data-ttu-id="9532e-108">O grupo não pode ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="9532e-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="9532e-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="9532e-109">FALSE</span></span>  <br/> |<span data-ttu-id="9532e-110">O grupo pode ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="9532e-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9532e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9532e-111">Remarks</span></span>

<span data-ttu-id="9532e-112">A definição do valor LockGroupCell como TRUE também impede a exclusão de formas que sejam membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="9532e-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="9532e-113">Para obter uma referência para a célula LockGroup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9532e-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9532e-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9532e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="9532e-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="9532e-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="9532e-116">Para obter uma referência para a célula LockGroup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9532e-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9532e-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9532e-117">Section index:</span></span>  <br/> |<span data-ttu-id="9532e-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9532e-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9532e-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9532e-119">Row index:</span></span>  <br/> |<span data-ttu-id="9532e-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9532e-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="9532e-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9532e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9532e-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="9532e-122">**visLockGroup**</span></span> <br/> |
   

