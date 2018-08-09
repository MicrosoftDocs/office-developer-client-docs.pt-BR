---
title: Célula YGridDensity (Seção Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica o tipo de grade vertical a ser utilizada.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773339"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="f15db-103">Célula YGridDensity (Seção Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="f15db-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="f15db-104">Especifica o tipo de grade vertical a ser utilizada.</span><span class="sxs-lookup"><span data-stu-id="f15db-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="f15db-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f15db-105">**Value**</span></span>|<span data-ttu-id="f15db-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f15db-106">**Description**</span></span>|<span data-ttu-id="f15db-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="f15db-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f15db-108">0</span><span class="sxs-lookup"><span data-stu-id="f15db-108">0</span></span>  <br/> |<span data-ttu-id="f15db-109">Fixa</span><span class="sxs-lookup"><span data-stu-id="f15db-109">Fixed</span></span>  <br/> |<span data-ttu-id="f15db-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="f15db-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="f15db-111">2</span><span class="sxs-lookup"><span data-stu-id="f15db-111">2</span></span>  <br/> |<span data-ttu-id="f15db-112">Grande</span><span class="sxs-lookup"><span data-stu-id="f15db-112">Coarse</span></span>  <br/> |<span data-ttu-id="f15db-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="f15db-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="f15db-114">4</span><span class="sxs-lookup"><span data-stu-id="f15db-114">4</span></span>  <br/> |<span data-ttu-id="f15db-115">Normal (padrão)</span><span class="sxs-lookup"><span data-stu-id="f15db-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="f15db-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="f15db-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="f15db-117">8</span><span class="sxs-lookup"><span data-stu-id="f15db-117">8</span></span>  <br/> |<span data-ttu-id="f15db-118">Pequena</span><span class="sxs-lookup"><span data-stu-id="f15db-118">Fine</span></span>  <br/> |<span data-ttu-id="f15db-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="f15db-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f15db-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f15db-120">Remarks</span></span>

<span data-ttu-id="f15db-121">Essa célula corresponde ao **espaçamento da grade** vertical opção no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="f15db-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="f15db-122">Para obter uma referência para a célula YGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f15db-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f15db-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f15db-123">Cell name:</span></span>  <br/> |<span data-ttu-id="f15db-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="f15db-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="f15db-125">Para obter uma referência para a célula YGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f15db-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f15db-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f15db-126">Section index:</span></span>  <br/> |<span data-ttu-id="f15db-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f15db-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f15db-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f15db-128">Row index:</span></span>  <br/> |<span data-ttu-id="f15db-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="f15db-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="f15db-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f15db-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f15db-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="f15db-131">**visYGridDensity**</span></span> <br/> |
   

