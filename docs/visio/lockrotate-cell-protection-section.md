---
title: Célula LockRotate (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Trava as formas 2D para impedir que sejam giradas com a alça de rotação ou com o comando Girar 90° para a esquerda ou Girar 90° para a direita.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348269"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="70cd4-103">Célula LockRotate (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="70cd4-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="70cd4-104">Trava as formas 2D para impedir que sejam giradas com a alça de rotação ou com o comando **Girar 90° para a esquerda** ou **Girar 90° para a direita**.</span><span class="sxs-lookup"><span data-stu-id="70cd4-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="70cd4-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="70cd4-105">**Value**</span></span>|<span data-ttu-id="70cd4-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="70cd4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="70cd4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="70cd4-107">TRUE</span></span>  <br/> | <span data-ttu-id="70cd4-108">A forma não pode ser girada.</span><span class="sxs-lookup"><span data-stu-id="70cd4-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="70cd4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="70cd4-109">FALSE</span></span>  <br/> | <span data-ttu-id="70cd4-110">A forma pode ser girada (padrão).</span><span class="sxs-lookup"><span data-stu-id="70cd4-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70cd4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="70cd4-111">Remarks</span></span>

<span data-ttu-id="70cd4-p101">A célula LockRotate não impedirá uma forma 1D de ser girada quando um ponto de extremidade for arrastado. Para proteger uma forma 1D contra a rotação, defina a célula LockWidth como um valor diferente de zero (VERDADEIRO).</span><span class="sxs-lookup"><span data-stu-id="70cd4-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="70cd4-114">Para fazer referência à célula LockRotate pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="70cd4-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70cd4-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="70cd4-115">Cell name:</span></span>  <br/> | <span data-ttu-id="70cd4-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="70cd4-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="70cd4-117">Para fazer referência à célula LockRotate pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="70cd4-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70cd4-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="70cd4-118">Section index:</span></span>  <br/> |<span data-ttu-id="70cd4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="70cd4-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="70cd4-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="70cd4-120">Row index:</span></span>  <br/> |<span data-ttu-id="70cd4-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="70cd4-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="70cd4-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="70cd4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="70cd4-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="70cd4-123">**visLockRotate**</span></span> <br/> |
   

