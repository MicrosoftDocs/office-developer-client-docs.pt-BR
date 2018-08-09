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
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773309"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="ae470-103">Célula XGridDensity (Seção Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="ae470-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="ae470-104">Especifica o tipo de grade horizontal a ser utilizada.</span><span class="sxs-lookup"><span data-stu-id="ae470-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="ae470-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae470-105">**Value**</span></span>|<span data-ttu-id="ae470-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae470-106">**Description**</span></span>|<span data-ttu-id="ae470-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="ae470-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae470-108">0</span><span class="sxs-lookup"><span data-stu-id="ae470-108">0</span></span>  <br/> |<span data-ttu-id="ae470-109">Fixa</span><span class="sxs-lookup"><span data-stu-id="ae470-109">Fixed</span></span>  <br/> |<span data-ttu-id="ae470-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="ae470-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="ae470-111">2</span><span class="sxs-lookup"><span data-stu-id="ae470-111">2</span></span>  <br/> |<span data-ttu-id="ae470-112">Grande</span><span class="sxs-lookup"><span data-stu-id="ae470-112">Coarse</span></span>  <br/> |<span data-ttu-id="ae470-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="ae470-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="ae470-114">4</span><span class="sxs-lookup"><span data-stu-id="ae470-114">4</span></span>  <br/> |<span data-ttu-id="ae470-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae470-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="ae470-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="ae470-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="ae470-117">8</span><span class="sxs-lookup"><span data-stu-id="ae470-117">8</span></span>  <br/> |<span data-ttu-id="ae470-118">Pequena</span><span class="sxs-lookup"><span data-stu-id="ae470-118">Fine</span></span>  <br/> |<span data-ttu-id="ae470-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="ae470-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae470-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae470-120">Remarks</span></span>

<span data-ttu-id="ae470-121">Essa célula corresponde ao **espaçamento da grade** horizontal opção no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="ae470-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="ae470-122">Para obter uma referência para a célula XGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ae470-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae470-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ae470-123">Cell name:</span></span>  <br/> |<span data-ttu-id="ae470-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="ae470-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="ae470-125">Para obter uma referência para a célula XGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ae470-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae470-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ae470-126">Section index:</span></span>  <br/> |<span data-ttu-id="ae470-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae470-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ae470-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ae470-128">Row index:</span></span>  <br/> |<span data-ttu-id="ae470-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="ae470-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="ae470-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ae470-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ae470-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="ae470-131">**visXGridDensity**</span></span> <br/> |
   

