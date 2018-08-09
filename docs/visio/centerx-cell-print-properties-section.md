---
title: Célula CenterX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Determina se a página de desenho ficará centralizada horizontalmente na página impressa.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771493"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="c62c6-103">Célula CenterX (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="c62c6-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="c62c6-104">Determina se a página de desenho ficará centralizada horizontalmente na página impressa.</span><span class="sxs-lookup"><span data-stu-id="c62c6-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="c62c6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c62c6-105">**Value**</span></span>|<span data-ttu-id="c62c6-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c62c6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c62c6-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c62c6-107">TRUE</span></span>  <br/> | <span data-ttu-id="c62c6-108">Centraliza a página de desenho horizontalmente na página impressa.</span><span class="sxs-lookup"><span data-stu-id="c62c6-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="c62c6-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="c62c6-109">FALSE</span></span>  <br/> | <span data-ttu-id="c62c6-110">Não centraliza a página de desenho horizontalmente na página impressa (o padrão).</span><span class="sxs-lookup"><span data-stu-id="c62c6-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c62c6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c62c6-111">Remarks</span></span>

<span data-ttu-id="c62c6-p101">Por padrão, as páginas de desenho são justificadas ao alto e à esquerda da página impressa. A configuração das células CenterX e CenterY como VERDADEIRO coloca a página de desenho no centro da página impressa (ou páginas quando for necessário colocar lado a lado).</span><span class="sxs-lookup"><span data-stu-id="c62c6-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="c62c6-114">Para fazer referência à célula CenterX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c62c6-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c62c6-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c62c6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c62c6-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="c62c6-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="c62c6-117">Para fazer referência à célula CenterX pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c62c6-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c62c6-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c62c6-118">Section index:</span></span>  <br/> |<span data-ttu-id="c62c6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c62c6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c62c6-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c62c6-120">Row index:</span></span>  <br/> |<span data-ttu-id="c62c6-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c62c6-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="c62c6-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c62c6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c62c6-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="c62c6-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

