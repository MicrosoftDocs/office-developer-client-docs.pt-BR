---
title: Célula XGridDensity (Seção Ruler &amp; Grid)
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436038"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="842bd-103">Célula XGridDensity (Seção Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="842bd-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="842bd-104">Especifica o tipo de grade horizontal a ser utilizada.</span><span class="sxs-lookup"><span data-stu-id="842bd-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="842bd-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="842bd-105">**Value**</span></span>|<span data-ttu-id="842bd-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="842bd-106">**Description**</span></span>|<span data-ttu-id="842bd-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="842bd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="842bd-108">0</span><span class="sxs-lookup"><span data-stu-id="842bd-108">0</span></span>  <br/> |<span data-ttu-id="842bd-109">Fixed</span><span class="sxs-lookup"><span data-stu-id="842bd-109">Fixed</span></span>  <br/> |<span data-ttu-id="842bd-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="842bd-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="842bd-111">2 </span><span class="sxs-lookup"><span data-stu-id="842bd-111">2</span></span>  <br/> |<span data-ttu-id="842bd-112">Insupernte</span><span class="sxs-lookup"><span data-stu-id="842bd-112">Coarse</span></span>  <br/> |<span data-ttu-id="842bd-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="842bd-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="842bd-114">4 </span><span class="sxs-lookup"><span data-stu-id="842bd-114">4</span></span>  <br/> |<span data-ttu-id="842bd-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="842bd-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="842bd-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="842bd-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="842bd-117">8 </span><span class="sxs-lookup"><span data-stu-id="842bd-117">8</span></span>  <br/> |<span data-ttu-id="842bd-118">Bem</span><span class="sxs-lookup"><span data-stu-id="842bd-118">Fine</span></span>  <br/> |<span data-ttu-id="842bd-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="842bd-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="842bd-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="842bd-120">Remarks</span></span>

<span data-ttu-id="842bd-121">Essa célula corresponde à opção de espaçamento **horizontal** Grid  na caixa de diálogo **Grade &amp;** de Régua (na guia Exibir, clique na **seta** Mostrar).</span><span class="sxs-lookup"><span data-stu-id="842bd-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="842bd-122">Para obter uma referência para a célula XGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="842bd-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="842bd-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="842bd-123">Cell name:</span></span>  <br/> |<span data-ttu-id="842bd-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="842bd-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="842bd-125">Para obter uma referência para a célula XGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="842bd-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="842bd-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="842bd-126">Section index:</span></span>  <br/> |<span data-ttu-id="842bd-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="842bd-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="842bd-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="842bd-128">Row index:</span></span>  <br/> |<span data-ttu-id="842bd-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="842bd-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="842bd-130">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="842bd-130">Cell index:</span></span>  <br/> |<span data-ttu-id="842bd-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="842bd-131">**visXGridDensity**</span></span> <br/> |
   

