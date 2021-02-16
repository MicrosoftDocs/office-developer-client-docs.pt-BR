---
title: Célula PrintPageOrientation (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Determina se a página será impressa na orientação retrato ou paisagem.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434862"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="c9f6e-103">Célula PrintPageOrientation (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="c9f6e-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="c9f6e-104">Determina se a página será impressa na orientação retrato ou paisagem.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="c9f6e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-105">**Value**</span></span>|<span data-ttu-id="c9f6e-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-106">**Orientation**</span></span>|<span data-ttu-id="c9f6e-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c9f6e-108">0</span><span class="sxs-lookup"><span data-stu-id="c9f6e-108">0</span></span>  <br/> | <span data-ttu-id="c9f6e-109">Mesmo que a impressora</span><span class="sxs-lookup"><span data-stu-id="c9f6e-109">Same as printer</span></span>  <br/> |<span data-ttu-id="c9f6e-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="c9f6e-111">1 </span><span class="sxs-lookup"><span data-stu-id="c9f6e-111">1</span></span>  <br/> | <span data-ttu-id="c9f6e-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="c9f6e-112">Portrait</span></span>  <br/> |<span data-ttu-id="c9f6e-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="c9f6e-114">2 </span><span class="sxs-lookup"><span data-stu-id="c9f6e-114">2</span></span>  <br/> |<span data-ttu-id="c9f6e-115">Paisagem</span><span class="sxs-lookup"><span data-stu-id="c9f6e-115">Landscape</span></span>  <br/> |<span data-ttu-id="c9f6e-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9f6e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9f6e-117">Remarks</span></span>

<span data-ttu-id="c9f6e-118">Quando você insere novas páginas em um documento, essa configuração assume como padrão a configuração na página ativa.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="c9f6e-119">Para fazer referência à célula PrintPageOrientation pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c9f6e-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9f6e-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c9f6e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="c9f6e-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="c9f6e-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="c9f6e-122">Para fazer referência à célula PrintPageOrientation pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c9f6e-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9f6e-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c9f6e-123">Section index:</span></span>  <br/> |<span data-ttu-id="c9f6e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c9f6e-125">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c9f6e-125">Row index:</span></span>  <br/> |<span data-ttu-id="c9f6e-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="c9f6e-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c9f6e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="c9f6e-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

