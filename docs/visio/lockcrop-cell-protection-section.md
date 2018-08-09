---
title: Célula LockCrop (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Protege um objeto de outro programa de ser recortado com a ferramenta Cortar.
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772240"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="14bf1-103">Célula LockCrop (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="14bf1-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="14bf1-104">Protege um objeto de outro programa de ser recortado com a ferramenta **Cortar**.</span><span class="sxs-lookup"><span data-stu-id="14bf1-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="14bf1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="14bf1-105">**Value**</span></span>|<span data-ttu-id="14bf1-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="14bf1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="14bf1-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="14bf1-107">TRUE</span></span>  <br/> | <span data-ttu-id="14bf1-108">A forma não pode ser cortada.</span><span class="sxs-lookup"><span data-stu-id="14bf1-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="14bf1-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="14bf1-109">FALSE</span></span>  <br/> | <span data-ttu-id="14bf1-110">A forma pode ser cortada.</span><span class="sxs-lookup"><span data-stu-id="14bf1-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14bf1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="14bf1-111">Remarks</span></span>

<span data-ttu-id="14bf1-112">Para fazer referência à célula LockCrop pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="14bf1-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14bf1-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="14bf1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="14bf1-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="14bf1-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="14bf1-115">Para fazer referência à célula LockCrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="14bf1-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14bf1-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="14bf1-116">Section index:</span></span>  <br/> |<span data-ttu-id="14bf1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="14bf1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="14bf1-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="14bf1-118">Row index:</span></span>  <br/> |<span data-ttu-id="14bf1-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="14bf1-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="14bf1-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="14bf1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="14bf1-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="14bf1-121">**visLockCrop**</span></span> <br/> |
   

