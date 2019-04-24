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
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341535"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="df653-103">Célula Alignment (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="df653-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="df653-104">Especifica o alinhamento de tabulação.</span><span class="sxs-lookup"><span data-stu-id="df653-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="df653-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="df653-105">**Value**</span></span>|<span data-ttu-id="df653-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="df653-106">**Alignment**</span></span>|<span data-ttu-id="df653-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="df653-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="df653-108">,0</span><span class="sxs-lookup"><span data-stu-id="df653-108">0</span></span>  <br/> | <span data-ttu-id="df653-109">Esquerda</span><span class="sxs-lookup"><span data-stu-id="df653-109">Left</span></span>  <br/> |<span data-ttu-id="df653-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="df653-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="df653-111">1</span><span class="sxs-lookup"><span data-stu-id="df653-111">1</span></span>  <br/> | <span data-ttu-id="df653-112">Centro</span><span class="sxs-lookup"><span data-stu-id="df653-112">Center</span></span>  <br/> |<span data-ttu-id="df653-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="df653-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="df653-114">duas</span><span class="sxs-lookup"><span data-stu-id="df653-114">2</span></span>  <br/> | <span data-ttu-id="df653-115">À direita</span><span class="sxs-lookup"><span data-stu-id="df653-115">Right</span></span>  <br/> |<span data-ttu-id="df653-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="df653-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="df653-117">3D</span><span class="sxs-lookup"><span data-stu-id="df653-117">3</span></span>  <br/> | <span data-ttu-id="df653-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="df653-118">Decimal</span></span>  <br/> |<span data-ttu-id="df653-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="df653-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="df653-120">quatro</span><span class="sxs-lookup"><span data-stu-id="df653-120">4</span></span>  <br/> | <span data-ttu-id="df653-121">Ponto</span><span class="sxs-lookup"><span data-stu-id="df653-121">Comma</span></span>  <br/> |<span data-ttu-id="df653-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="df653-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df653-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="df653-123">Remarks</span></span>

<span data-ttu-id="df653-124">Para fazer referência à célula Alignment pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="df653-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df653-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="df653-125">Cell name:</span></span>  <br/> | <span data-ttu-id="df653-126">Tabula.</span><span class="sxs-lookup"><span data-stu-id="df653-126">Tabs.</span></span>  <span data-ttu-id="df653-127">*IJ* onde *i e j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="df653-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="df653-128">Para fazer referência à célula Alignment pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="df653-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df653-129">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="df653-129">Section index:</span></span>  <br/> |<span data-ttu-id="df653-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="df653-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="df653-131">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="df653-131">Row index:</span></span>  <br/> |<span data-ttu-id="df653-132">**visRowTab +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="df653-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="df653-133">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="df653-133">Cell index:</span></span>  <br/> | <span data-ttu-id="df653-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="df653-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

