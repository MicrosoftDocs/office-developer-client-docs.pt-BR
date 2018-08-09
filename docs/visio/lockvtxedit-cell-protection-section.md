---
title: Célula LockVtxEdit (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Protege os vértices de uma forma impedindo-a de ser editada.
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772285"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="9a902-103">Célula LockVtxEdit (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="9a902-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="9a902-104">Protege os vértices de uma forma impedindo-a de ser editada.</span><span class="sxs-lookup"><span data-stu-id="9a902-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="9a902-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9a902-105">**Value**</span></span>|<span data-ttu-id="9a902-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a902-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a902-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="9a902-107">TRUE</span></span>  <br/> |<span data-ttu-id="9a902-108">Os vértices não podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="9a902-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="9a902-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="9a902-109">FALSE</span></span>  <br/> |<span data-ttu-id="9a902-110">Os vértices podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="9a902-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a902-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a902-111">Remarks</span></span>

<span data-ttu-id="9a902-112">Para obter uma referência para a célula LockVtxEdit pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9a902-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a902-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9a902-113">Cell name:</span></span>  <br/> |<span data-ttu-id="9a902-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="9a902-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="9a902-115">Para obter uma referência para a célula LockVtxEdit pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9a902-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a902-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9a902-116">Section index:</span></span>  <br/> |<span data-ttu-id="9a902-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9a902-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9a902-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9a902-118">Row index:</span></span>  <br/> |<span data-ttu-id="9a902-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9a902-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="9a902-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9a902-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9a902-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="9a902-121">**visLockVtxEdit**</span></span> <br/> |
   

