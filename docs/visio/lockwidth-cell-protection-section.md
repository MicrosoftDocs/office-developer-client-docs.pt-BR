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
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439804"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="eb4d6-103">Célula LockWidth (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="eb4d6-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="eb4d6-104">Protege a largura da forma para que ela não seja alterada quando a forma for dimensionada.</span><span class="sxs-lookup"><span data-stu-id="eb4d6-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="eb4d6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="eb4d6-105">**Value**</span></span>|<span data-ttu-id="eb4d6-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eb4d6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eb4d6-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="eb4d6-107">TRUE</span></span>  <br/> | <span data-ttu-id="eb4d6-108">A largura está protegida.</span><span class="sxs-lookup"><span data-stu-id="eb4d6-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="eb4d6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eb4d6-109">FALSE</span></span>  <br/> | <span data-ttu-id="eb4d6-110">A largura não está protegida.</span><span class="sxs-lookup"><span data-stu-id="eb4d6-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb4d6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb4d6-111">Remarks</span></span>

<span data-ttu-id="eb4d6-112">Para fazer referência à célula LockWidth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="eb4d6-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb4d6-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="eb4d6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="eb4d6-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="eb4d6-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="eb4d6-115">Para fazer referência à célula LockWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="eb4d6-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb4d6-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="eb4d6-116">Section index:</span></span>  <br/> |<span data-ttu-id="eb4d6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb4d6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb4d6-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="eb4d6-118">Row index:</span></span>  <br/> |<span data-ttu-id="eb4d6-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="eb4d6-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="eb4d6-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="eb4d6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="eb4d6-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="eb4d6-121">**visLockWidth**</span></span> <br/> |
   

