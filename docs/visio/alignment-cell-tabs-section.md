---
title: Célula Alignment (Seção Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Especifica o alinhamento de tabulação.
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771254"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="2f125-103">Célula Alignment (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="2f125-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="2f125-104">Especifica o alinhamento de tabulação.</span><span class="sxs-lookup"><span data-stu-id="2f125-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="2f125-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2f125-105">**Value**</span></span>|<span data-ttu-id="2f125-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="2f125-106">**Alignment**</span></span>|<span data-ttu-id="2f125-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="2f125-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2f125-108">0</span><span class="sxs-lookup"><span data-stu-id="2f125-108">0</span></span>  <br/> | <span data-ttu-id="2f125-109">À esquerda</span><span class="sxs-lookup"><span data-stu-id="2f125-109">Left</span></span>  <br/> |<span data-ttu-id="2f125-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="2f125-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="2f125-111">1</span><span class="sxs-lookup"><span data-stu-id="2f125-111">1</span></span>  <br/> | <span data-ttu-id="2f125-112">Centralizar</span><span class="sxs-lookup"><span data-stu-id="2f125-112">Center</span></span>  <br/> |<span data-ttu-id="2f125-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="2f125-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="2f125-114">2</span><span class="sxs-lookup"><span data-stu-id="2f125-114">2</span></span>  <br/> | <span data-ttu-id="2f125-115">Direita</span><span class="sxs-lookup"><span data-stu-id="2f125-115">Right</span></span>  <br/> |<span data-ttu-id="2f125-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="2f125-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="2f125-117">3</span><span class="sxs-lookup"><span data-stu-id="2f125-117">3</span></span>  <br/> | <span data-ttu-id="2f125-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="2f125-118">Decimal</span></span>  <br/> |<span data-ttu-id="2f125-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="2f125-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="2f125-120">4</span><span class="sxs-lookup"><span data-stu-id="2f125-120">4</span></span>  <br/> | <span data-ttu-id="2f125-121">Vírgula</span><span class="sxs-lookup"><span data-stu-id="2f125-121">Comma</span></span>  <br/> |<span data-ttu-id="2f125-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="2f125-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f125-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f125-123">Remarks</span></span>

<span data-ttu-id="2f125-124">Para fazer referência à célula Alignment pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2f125-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f125-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2f125-125">Cell name:</span></span>  <br/> | <span data-ttu-id="2f125-126">Guias.</span><span class="sxs-lookup"><span data-stu-id="2f125-126">Tabs.</span></span>  <span data-ttu-id="2f125-127">*ij* onde *i e j =* < 1 >, 2, 3</span><span class="sxs-lookup"><span data-stu-id="2f125-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="2f125-128">Para fazer referência à célula Alignment pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2f125-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f125-129">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2f125-129">Section index:</span></span>  <br/> |<span data-ttu-id="2f125-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="2f125-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="2f125-131">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2f125-131">Row index:</span></span>  <br/> |<span data-ttu-id="2f125-132">**visRowTab +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2f125-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2f125-133">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2f125-133">Cell index:</span></span>  <br/> | <span data-ttu-id="2f125-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="2f125-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

