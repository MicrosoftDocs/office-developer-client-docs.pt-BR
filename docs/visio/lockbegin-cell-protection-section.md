---
title: Célula LockBegin (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Protege o ponto inicial (BeginX, BeginY) de uma forma 1D para uma localização específica.
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772228"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="4fe48-103">Célula LockBegin (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="4fe48-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="4fe48-104">Protege o ponto inicial (BeginX, BeginY) de uma forma 1D para uma localização específica.</span><span class="sxs-lookup"><span data-stu-id="4fe48-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="4fe48-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4fe48-105">**Value**</span></span>|<span data-ttu-id="4fe48-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4fe48-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4fe48-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="4fe48-107">TRUE</span></span>  <br/> | <span data-ttu-id="4fe48-108">O ponto inicial está protegido.</span><span class="sxs-lookup"><span data-stu-id="4fe48-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="4fe48-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="4fe48-109">FALSE</span></span>  <br/> | <span data-ttu-id="4fe48-110">O ponto inicial não está protegido.</span><span class="sxs-lookup"><span data-stu-id="4fe48-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fe48-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fe48-111">Remarks</span></span>

<span data-ttu-id="4fe48-112">Para fazer referência à célula LockBegin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4fe48-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4fe48-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4fe48-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4fe48-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="4fe48-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="4fe48-115">Para fazer referência à célula LockBegin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4fe48-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4fe48-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4fe48-116">Section index:</span></span>  <br/> |<span data-ttu-id="4fe48-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4fe48-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4fe48-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4fe48-118">Row index:</span></span>  <br/> |<span data-ttu-id="4fe48-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4fe48-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="4fe48-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4fe48-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4fe48-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="4fe48-121">**visLockBegin**</span></span> <br/> |
   

