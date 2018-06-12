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
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="e111c-103">Célula Alignment (Seção Tabs)</span><span class="sxs-lookup"><span data-stu-id="e111c-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="e111c-104">Especifica o alinhamento de tabulação.</span><span class="sxs-lookup"><span data-stu-id="e111c-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="e111c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e111c-105">**Value**</span></span>|<span data-ttu-id="e111c-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="e111c-106">**Alignment**</span></span>|<span data-ttu-id="e111c-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e111c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e111c-108">0</span><span class="sxs-lookup"><span data-stu-id="e111c-108">0</span></span>  <br/> | <span data-ttu-id="e111c-109">À esquerda</span><span class="sxs-lookup"><span data-stu-id="e111c-109">Left</span></span>  <br/> |<span data-ttu-id="e111c-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="e111c-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="e111c-111">1</span><span class="sxs-lookup"><span data-stu-id="e111c-111">1</span></span>  <br/> | <span data-ttu-id="e111c-112">Centralizar</span><span class="sxs-lookup"><span data-stu-id="e111c-112">Center</span></span>  <br/> |<span data-ttu-id="e111c-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="e111c-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="e111c-114">2</span><span class="sxs-lookup"><span data-stu-id="e111c-114">2</span></span>  <br/> | <span data-ttu-id="e111c-115">À direita</span><span class="sxs-lookup"><span data-stu-id="e111c-115">Right</span></span>  <br/> |<span data-ttu-id="e111c-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="e111c-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="e111c-117">3</span><span class="sxs-lookup"><span data-stu-id="e111c-117">3</span></span>  <br/> | <span data-ttu-id="e111c-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="e111c-118">Decimal</span></span>  <br/> |<span data-ttu-id="e111c-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="e111c-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="e111c-120">4</span><span class="sxs-lookup"><span data-stu-id="e111c-120">4</span></span>  <br/> | <span data-ttu-id="e111c-121">Vírgula</span><span class="sxs-lookup"><span data-stu-id="e111c-121">Comma</span></span>  <br/> |<span data-ttu-id="e111c-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="e111c-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e111c-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e111c-123">Remarks</span></span>

<span data-ttu-id="e111c-124">Para obter uma referência à célula Alignment pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="e111c-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e111c-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e111c-125">Cell name:</span></span>  <br/> | <span data-ttu-id="e111c-126">Guias.</span><span class="sxs-lookup"><span data-stu-id="e111c-126">Tabs.</span></span>  <span data-ttu-id="e111c-127">*ij* onde *i e j =* < 1 >, 2, 3</span><span class="sxs-lookup"><span data-stu-id="e111c-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="e111c-128">Para obter uma referência à célula Alignment pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e111c-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e111c-129">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e111c-129">Section index:</span></span>  <br/> |<span data-ttu-id="e111c-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="e111c-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="e111c-131">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e111c-131">Row index:</span></span>  <br/> |<span data-ttu-id="e111c-132">**visRowTab +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e111c-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e111c-133">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e111c-133">Cell index:</span></span>  <br/> | <span data-ttu-id="e111c-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="e111c-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

