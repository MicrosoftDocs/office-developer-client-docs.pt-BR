---
title: Célula XRulerDensity (seção Ruler &amp; seção grade)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica as subdivisões horizontais da régua na página.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773305"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="9c57b-103">Célula XRulerDensity (seção Ruler &amp; seção grade)</span><span class="sxs-lookup"><span data-stu-id="9c57b-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="9c57b-104">Especifica as subdivisões horizontais da régua na página.</span><span class="sxs-lookup"><span data-stu-id="9c57b-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="9c57b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9c57b-105">**Value**</span></span>|<span data-ttu-id="9c57b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9c57b-106">**Description**</span></span>|<span data-ttu-id="9c57b-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="9c57b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c57b-108">0</span><span class="sxs-lookup"><span data-stu-id="9c57b-108">0</span></span>  <br/> |<span data-ttu-id="9c57b-109">Fixa</span><span class="sxs-lookup"><span data-stu-id="9c57b-109">Fixed</span></span>  <br/> |<span data-ttu-id="9c57b-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="9c57b-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="9c57b-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="9c57b-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="9c57b-112">Grande</span><span class="sxs-lookup"><span data-stu-id="9c57b-112">Coarse</span></span>  <br/> |<span data-ttu-id="9c57b-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="9c57b-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="9c57b-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="9c57b-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="9c57b-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c57b-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="9c57b-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="9c57b-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="9c57b-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="9c57b-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="9c57b-118">Pequena</span><span class="sxs-lookup"><span data-stu-id="9c57b-118">Fine</span></span>  <br/> |<span data-ttu-id="9c57b-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="9c57b-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c57b-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="9c57b-120">Remarks</span></span>

<span data-ttu-id="9c57b-121">Essa célula corresponde à opção horizontal **Subdivisões** no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="9c57b-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="9c57b-122">Para obter uma referência para a célula XRulerDensity pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="9c57b-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c57b-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9c57b-123">Cell name:</span></span>  <br/> |<span data-ttu-id="9c57b-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="9c57b-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="9c57b-125">Para obter uma referência para a célula XRulerDensity pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9c57b-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c57b-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9c57b-126">Section index:</span></span>  <br/> |<span data-ttu-id="9c57b-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9c57b-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9c57b-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9c57b-128">Row index:</span></span>  <br/> |<span data-ttu-id="9c57b-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="9c57b-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="9c57b-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9c57b-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9c57b-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="9c57b-131">**visXRulerDensity**</span></span> <br/> |
   

