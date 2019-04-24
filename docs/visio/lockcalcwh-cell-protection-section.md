---
title: Célula LockCalcWH (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Bloqueia um retângulo de seleção de uma forma para que ele não seja recalculado quando uma vértice for editada ou um tipo de linha for alterado na seção Geometry.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359630"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="0a4a5-103">Célula LockCalcWH (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="0a4a5-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="0a4a5-104">Bloqueia um retângulo de seleção de uma forma para que ele não seja recalculado quando uma vértice for editada ou um tipo de linha for alterado na seção Geometry.</span><span class="sxs-lookup"><span data-stu-id="0a4a5-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="0a4a5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0a4a5-105">**Value**</span></span>|<span data-ttu-id="0a4a5-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0a4a5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0a4a5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0a4a5-107">TRUE</span></span>  <br/> | <span data-ttu-id="0a4a5-108">A largura e a altura não podem ser recalculadas.</span><span class="sxs-lookup"><span data-stu-id="0a4a5-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="0a4a5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0a4a5-109">FALSE</span></span>  <br/> | <span data-ttu-id="0a4a5-110">A largura e a altura podem ser recalculadas.</span><span class="sxs-lookup"><span data-stu-id="0a4a5-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a4a5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a4a5-111">Remarks</span></span>

<span data-ttu-id="0a4a5-112">Para fazer referência à célula LockCalcWH pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0a4a5-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a4a5-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0a4a5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0a4a5-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="0a4a5-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="0a4a5-115">Para fazer referência à célula LockCalcWH pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0a4a5-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a4a5-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0a4a5-116">Section index:</span></span>  <br/> |<span data-ttu-id="0a4a5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a4a5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0a4a5-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0a4a5-118">Row index:</span></span>  <br/> |<span data-ttu-id="0a4a5-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="0a4a5-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="0a4a5-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0a4a5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0a4a5-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="0a4a5-121">**visLockCalcWH**</span></span> <br/> |
   

