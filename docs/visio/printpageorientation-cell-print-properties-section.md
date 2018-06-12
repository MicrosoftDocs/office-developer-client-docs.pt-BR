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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772607"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="d3dc1-103">Célula PrintPageOrientation (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="d3dc1-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="d3dc1-104">Determina se a página será impressa na orientação retrato ou paisagem.</span><span class="sxs-lookup"><span data-stu-id="d3dc1-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="d3dc1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-105">**Value**</span></span>|<span data-ttu-id="d3dc1-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-106">**Orientation**</span></span>|<span data-ttu-id="d3dc1-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d3dc1-108">0</span><span class="sxs-lookup"><span data-stu-id="d3dc1-108">0</span></span>  <br/> | <span data-ttu-id="d3dc1-109">Mesmo que a impressora</span><span class="sxs-lookup"><span data-stu-id="d3dc1-109">Same as printer</span></span>  <br/> |<span data-ttu-id="d3dc1-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="d3dc1-111">1</span><span class="sxs-lookup"><span data-stu-id="d3dc1-111">1</span></span>  <br/> | <span data-ttu-id="d3dc1-112">Retrato</span><span class="sxs-lookup"><span data-stu-id="d3dc1-112">Portrait</span></span>  <br/> |<span data-ttu-id="d3dc1-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="d3dc1-114">2</span><span class="sxs-lookup"><span data-stu-id="d3dc1-114">2</span></span>  <br/> |<span data-ttu-id="d3dc1-115">Paisagem</span><span class="sxs-lookup"><span data-stu-id="d3dc1-115">Landscape</span></span>  <br/> |<span data-ttu-id="d3dc1-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3dc1-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d3dc1-117">Remarks</span></span>

<span data-ttu-id="d3dc1-118">Quando você insere novas páginas em um documento, essa configuração padrão é a configuração da página ativa.</span><span class="sxs-lookup"><span data-stu-id="d3dc1-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="d3dc1-119">Para obter uma referência à célula PrintPageOrientation pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d3dc1-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3dc1-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d3dc1-120">Cell name:</span></span>  <br/> | <span data-ttu-id="d3dc1-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="d3dc1-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="d3dc1-122">Para obter uma referência à célula PrintPageOrientation pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d3dc1-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3dc1-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d3dc1-123">Section index:</span></span>  <br/> |<span data-ttu-id="d3dc1-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d3dc1-125">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d3dc1-125">Row index:</span></span>  <br/> |<span data-ttu-id="d3dc1-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d3dc1-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d3dc1-127">Cell index:</span></span>  <br/> |<span data-ttu-id="d3dc1-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="d3dc1-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

