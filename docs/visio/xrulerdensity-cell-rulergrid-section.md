---
title: Célula XRulerDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica as subdivisões horizontais da régua na página.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411467"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="0de06-103">Célula XRulerDensity (seção &amp; Ruler Grid)</span><span class="sxs-lookup"><span data-stu-id="0de06-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="0de06-104">Especifica as subdivisões horizontais da régua na página.</span><span class="sxs-lookup"><span data-stu-id="0de06-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="0de06-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0de06-105">**Value**</span></span>|<span data-ttu-id="0de06-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0de06-106">**Description**</span></span>|<span data-ttu-id="0de06-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="0de06-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0de06-108">,0</span><span class="sxs-lookup"><span data-stu-id="0de06-108">0</span></span>  <br/> |<span data-ttu-id="0de06-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="0de06-109">Fixed</span></span>  <br/> |<span data-ttu-id="0de06-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="0de06-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="0de06-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="0de06-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="0de06-112">Grande</span><span class="sxs-lookup"><span data-stu-id="0de06-112">Coarse</span></span>  <br/> |<span data-ttu-id="0de06-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="0de06-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="0de06-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="0de06-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="0de06-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="0de06-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="0de06-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="0de06-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="0de06-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="0de06-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="0de06-118">Funciona</span><span class="sxs-lookup"><span data-stu-id="0de06-118">Fine</span></span>  <br/> |<span data-ttu-id="0de06-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="0de06-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0de06-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0de06-120">Remarks</span></span>

<span data-ttu-id="0de06-121">Esta célula corresponde à opção horizontal **subdivisões** da caixa de diálogo **grade da &amp; régua** (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="0de06-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="0de06-122">Para obter uma referência para a célula XRulerDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0de06-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0de06-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0de06-123">Cell name:</span></span>  <br/> |<span data-ttu-id="0de06-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="0de06-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="0de06-125">Para obter uma referência para a célula XRulerDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0de06-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0de06-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0de06-126">Section index:</span></span>  <br/> |<span data-ttu-id="0de06-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0de06-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0de06-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="0de06-128">Row index:</span></span>  <br/> |<span data-ttu-id="0de06-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="0de06-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="0de06-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0de06-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0de06-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="0de06-131">**visXRulerDensity**</span></span> <br/> |
   

