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
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="50933-103">Célula LockGroup (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="50933-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="50933-104">Protege um grupo impedindo-o de ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="50933-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="50933-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="50933-105">**Value**</span></span>|<span data-ttu-id="50933-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50933-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50933-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="50933-107">TRUE</span></span>  <br/> |<span data-ttu-id="50933-108">O grupo não pode ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="50933-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="50933-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="50933-109">FALSE</span></span>  <br/> |<span data-ttu-id="50933-110">O grupo pode ser desagrupado.</span><span class="sxs-lookup"><span data-stu-id="50933-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50933-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="50933-111">Remarks</span></span>

<span data-ttu-id="50933-112">A definição do valor LockGroupCell como TRUE também impede a exclusão de formas que sejam membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="50933-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="50933-113">Para obter uma referência para a célula LockGroup pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="50933-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50933-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="50933-114">Cell name:</span></span>  <br/> |<span data-ttu-id="50933-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="50933-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="50933-116">Para obter uma referência para a célula LockGroup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="50933-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50933-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="50933-117">Section index:</span></span>  <br/> |<span data-ttu-id="50933-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50933-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="50933-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="50933-119">Row index:</span></span>  <br/> |<span data-ttu-id="50933-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="50933-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="50933-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="50933-121">Cell index:</span></span>  <br/> |<span data-ttu-id="50933-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="50933-122">**visLockGroup**</span></span> <br/> |
   

