---
title: Célula LockHeight (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Protege a altura da forma para que ela não seja alterada quando a forma for dimensionada.
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772252"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="9e9aa-103">Célula LockHeight (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="9e9aa-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="9e9aa-104">Protege a altura da forma para que ela não seja alterada quando a forma for dimensionada.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="9e9aa-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9e9aa-105">**Value**</span></span>|<span data-ttu-id="9e9aa-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9e9aa-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9e9aa-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="9e9aa-107">TRUE</span></span>  <br/> | <span data-ttu-id="9e9aa-108">A altura está protegida.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="9e9aa-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="9e9aa-109">FALSE</span></span>  <br/> | <span data-ttu-id="9e9aa-110">A altura não está protegida.</span><span class="sxs-lookup"><span data-stu-id="9e9aa-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e9aa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e9aa-111">Remarks</span></span>

<span data-ttu-id="9e9aa-112">Para fazer referência à célula LockHeight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9e9aa-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e9aa-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9e9aa-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9e9aa-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="9e9aa-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="9e9aa-115">Para fazer referência à célula LockHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9e9aa-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e9aa-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9e9aa-116">Section index:</span></span>  <br/> |<span data-ttu-id="9e9aa-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e9aa-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9e9aa-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9e9aa-118">Row index:</span></span>  <br/> |<span data-ttu-id="9e9aa-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9e9aa-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="9e9aa-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9e9aa-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9e9aa-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="9e9aa-121">**visLockHeight**</span></span> <br/> |
   

