---
title: Célula LockWidth (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Protege a largura da forma para que ela não seja alterada quando a forma for dimensionada.
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772277"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="7aafa-103">Célula LockWidth (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="7aafa-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="7aafa-104">Protege a largura da forma para que ela não seja alterada quando a forma for dimensionada.</span><span class="sxs-lookup"><span data-stu-id="7aafa-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="7aafa-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7aafa-105">**Value**</span></span>|<span data-ttu-id="7aafa-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7aafa-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7aafa-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="7aafa-107">TRUE</span></span>  <br/> | <span data-ttu-id="7aafa-108">A largura está protegida.</span><span class="sxs-lookup"><span data-stu-id="7aafa-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="7aafa-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="7aafa-109">FALSE</span></span>  <br/> | <span data-ttu-id="7aafa-110">A largura não está protegida.</span><span class="sxs-lookup"><span data-stu-id="7aafa-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7aafa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7aafa-111">Remarks</span></span>

<span data-ttu-id="7aafa-112">Para fazer referência à célula LockWidth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7aafa-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7aafa-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7aafa-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7aafa-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="7aafa-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="7aafa-115">Para fazer referência à célula LockWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7aafa-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7aafa-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7aafa-116">Section index:</span></span>  <br/> |<span data-ttu-id="7aafa-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7aafa-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7aafa-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7aafa-118">Row index:</span></span>  <br/> |<span data-ttu-id="7aafa-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="7aafa-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="7aafa-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7aafa-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7aafa-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="7aafa-121">**visLockWidth**</span></span> <br/> |
   

