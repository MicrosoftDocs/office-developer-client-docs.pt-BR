---
title: Célula XGridDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica o tipo de grade horizontal a ser utilizada.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328975"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="3a5ba-103">Célula XGridDensity (seção &amp; Ruler Grid)</span><span class="sxs-lookup"><span data-stu-id="3a5ba-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="3a5ba-104">Especifica o tipo de grade horizontal a ser utilizada.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="3a5ba-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-105">**Value**</span></span>|<span data-ttu-id="3a5ba-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-106">**Description**</span></span>|<span data-ttu-id="3a5ba-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3a5ba-108">,0</span><span class="sxs-lookup"><span data-stu-id="3a5ba-108">0</span></span>  <br/> |<span data-ttu-id="3a5ba-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="3a5ba-109">Fixed</span></span>  <br/> |<span data-ttu-id="3a5ba-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="3a5ba-111">duas</span><span class="sxs-lookup"><span data-stu-id="3a5ba-111">2</span></span>  <br/> |<span data-ttu-id="3a5ba-112">Grande</span><span class="sxs-lookup"><span data-stu-id="3a5ba-112">Coarse</span></span>  <br/> |<span data-ttu-id="3a5ba-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="3a5ba-114">quatro</span><span class="sxs-lookup"><span data-stu-id="3a5ba-114">4</span></span>  <br/> |<span data-ttu-id="3a5ba-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a5ba-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="3a5ba-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="3a5ba-117">8</span><span class="sxs-lookup"><span data-stu-id="3a5ba-117">8</span></span>  <br/> |<span data-ttu-id="3a5ba-118">Funciona</span><span class="sxs-lookup"><span data-stu-id="3a5ba-118">Fine</span></span>  <br/> |<span data-ttu-id="3a5ba-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a5ba-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a5ba-120">Remarks</span></span>

<span data-ttu-id="3a5ba-121">Esta célula corresponde à opção horizontal **espaçamento da grade** na caixa de diálogo **grade da &amp; régua** (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="3a5ba-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="3a5ba-122">Para obter uma referência para a célula XGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3a5ba-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a5ba-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3a5ba-123">Cell name:</span></span>  <br/> |<span data-ttu-id="3a5ba-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="3a5ba-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="3a5ba-125">Para obter uma referência para a célula XGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3a5ba-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a5ba-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3a5ba-126">Section index:</span></span>  <br/> |<span data-ttu-id="3a5ba-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3a5ba-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="3a5ba-128">Row index:</span></span>  <br/> |<span data-ttu-id="3a5ba-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="3a5ba-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3a5ba-130">Cell index:</span></span>  <br/> |<span data-ttu-id="3a5ba-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="3a5ba-131">**visXGridDensity**</span></span> <br/> |
   

