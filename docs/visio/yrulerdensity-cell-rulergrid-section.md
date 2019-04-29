---
title: Célula YRulerDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica as subdivisões verticais da régua na página.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406798"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="e69ec-103">Célula YRulerDensity (seção &amp; Ruler Grid)</span><span class="sxs-lookup"><span data-stu-id="e69ec-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="e69ec-104">Especifica as subdivisões verticais da régua na página.</span><span class="sxs-lookup"><span data-stu-id="e69ec-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="e69ec-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e69ec-105">**Value**</span></span>|<span data-ttu-id="e69ec-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e69ec-106">**Description**</span></span>|<span data-ttu-id="e69ec-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e69ec-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e69ec-108">,0</span><span class="sxs-lookup"><span data-stu-id="e69ec-108">0</span></span>  <br/> |<span data-ttu-id="e69ec-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="e69ec-109">Fixed</span></span>  <br/> |<span data-ttu-id="e69ec-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="e69ec-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="e69ec-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="e69ec-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="e69ec-112">Grande</span><span class="sxs-lookup"><span data-stu-id="e69ec-112">Coarse</span></span>  <br/> |<span data-ttu-id="e69ec-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="e69ec-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="e69ec-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="e69ec-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="e69ec-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="e69ec-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="e69ec-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="e69ec-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="e69ec-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="e69ec-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="e69ec-118">Funciona</span><span class="sxs-lookup"><span data-stu-id="e69ec-118">Fine</span></span>  <br/> |<span data-ttu-id="e69ec-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="e69ec-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e69ec-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e69ec-120">Remarks</span></span>

<span data-ttu-id="e69ec-121">Esta célula corresponde à opção de **subdivisões** verticais da caixa de diálogo **grade &amp; da régua** (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="e69ec-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="e69ec-122">Para obter uma referência para a célula YRulerDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e69ec-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e69ec-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e69ec-123">Cell name:</span></span>  <br/> |<span data-ttu-id="e69ec-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="e69ec-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="e69ec-125">Para obter uma referência para a célula YRulerDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e69ec-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e69ec-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e69ec-126">Section index:</span></span>  <br/> |<span data-ttu-id="e69ec-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e69ec-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e69ec-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="e69ec-128">Row index:</span></span>  <br/> |<span data-ttu-id="e69ec-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="e69ec-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="e69ec-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e69ec-130">Cell index:</span></span>  <br/> |<span data-ttu-id="e69ec-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="e69ec-131">**visYRulerDensity**</span></span> <br/> |
   

