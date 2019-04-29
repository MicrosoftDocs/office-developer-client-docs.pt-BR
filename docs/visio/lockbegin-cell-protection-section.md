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
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407757"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="b4152-103">Célula LockBegin (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="b4152-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="b4152-104">Protege o ponto inicial (BeginX, BeginY) de uma forma 1D para uma localização específica.</span><span class="sxs-lookup"><span data-stu-id="b4152-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="b4152-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b4152-105">**Value**</span></span>|<span data-ttu-id="b4152-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b4152-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b4152-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="b4152-107">TRUE</span></span>  <br/> | <span data-ttu-id="b4152-108">O ponto inicial está protegido.</span><span class="sxs-lookup"><span data-stu-id="b4152-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="b4152-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b4152-109">FALSE</span></span>  <br/> | <span data-ttu-id="b4152-110">O ponto inicial não está protegido.</span><span class="sxs-lookup"><span data-stu-id="b4152-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4152-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4152-111">Remarks</span></span>

<span data-ttu-id="b4152-112">Para fazer referência à célula LockBegin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b4152-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4152-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b4152-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b4152-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="b4152-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="b4152-115">Para fazer referência à célula LockBegin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b4152-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4152-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b4152-116">Section index:</span></span>  <br/> |<span data-ttu-id="b4152-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b4152-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b4152-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b4152-118">Row index:</span></span>  <br/> |<span data-ttu-id="b4152-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b4152-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b4152-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b4152-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b4152-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="b4152-121">**visLockBegin**</span></span> <br/> |
   

