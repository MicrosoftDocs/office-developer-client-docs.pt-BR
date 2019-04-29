---
title: Célula YGridDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica o tipo de grade vertical a ser utilizada.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429807"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="3bb6f-103">Célula YGridDensity (seção &amp; Ruler Grid)</span><span class="sxs-lookup"><span data-stu-id="3bb6f-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="3bb6f-104">Especifica o tipo de grade vertical a ser utilizada.</span><span class="sxs-lookup"><span data-stu-id="3bb6f-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="3bb6f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-105">**Value**</span></span>|<span data-ttu-id="3bb6f-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-106">**Description**</span></span>|<span data-ttu-id="3bb6f-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3bb6f-108">,0</span><span class="sxs-lookup"><span data-stu-id="3bb6f-108">0</span></span>  <br/> |<span data-ttu-id="3bb6f-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="3bb6f-109">Fixed</span></span>  <br/> |<span data-ttu-id="3bb6f-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="3bb6f-111">duas</span><span class="sxs-lookup"><span data-stu-id="3bb6f-111">2</span></span>  <br/> |<span data-ttu-id="3bb6f-112">Grande</span><span class="sxs-lookup"><span data-stu-id="3bb6f-112">Coarse</span></span>  <br/> |<span data-ttu-id="3bb6f-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="3bb6f-114">4 </span><span class="sxs-lookup"><span data-stu-id="3bb6f-114">4</span></span>  <br/> |<span data-ttu-id="3bb6f-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="3bb6f-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="3bb6f-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="3bb6f-117">8 </span><span class="sxs-lookup"><span data-stu-id="3bb6f-117">8</span></span>  <br/> |<span data-ttu-id="3bb6f-118">Funciona</span><span class="sxs-lookup"><span data-stu-id="3bb6f-118">Fine</span></span>  <br/> |<span data-ttu-id="3bb6f-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bb6f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bb6f-120">Remarks</span></span>

<span data-ttu-id="3bb6f-121">Esta célula corresponde à opção espaçamento da **grade** vertical da caixa de diálogo **grade da &amp; régua** (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="3bb6f-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="3bb6f-122">Para obter uma referência para a célula YGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3bb6f-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bb6f-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3bb6f-123">Cell name:</span></span>  <br/> |<span data-ttu-id="3bb6f-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="3bb6f-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="3bb6f-125">Para obter uma referência para a célula YGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3bb6f-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bb6f-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3bb6f-126">Section index:</span></span>  <br/> |<span data-ttu-id="3bb6f-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3bb6f-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3bb6f-128">Row index:</span></span>  <br/> |<span data-ttu-id="3bb6f-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="3bb6f-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3bb6f-130">Cell index:</span></span>  <br/> |<span data-ttu-id="3bb6f-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="3bb6f-131">**visYGridDensity**</span></span> <br/> |
   

