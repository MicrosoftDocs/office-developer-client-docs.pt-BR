---
title: Célula CenterY (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Determina se a página de desenho ficará centralizada verticalmente na página impressa.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771512"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="34917-103">Célula CenterY (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="34917-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="34917-104">Determina se a página de desenho ficará centralizada verticalmente na página impressa.</span><span class="sxs-lookup"><span data-stu-id="34917-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="34917-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="34917-105">**Value**</span></span>|<span data-ttu-id="34917-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34917-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="34917-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="34917-107">TRUE</span></span>  <br/> | <span data-ttu-id="34917-108">Centraliza a página de desenho verticalmente na página impressa.</span><span class="sxs-lookup"><span data-stu-id="34917-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="34917-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="34917-109">FALSE</span></span>  <br/> | <span data-ttu-id="34917-110">Não centraliza a página de desenho verticalmente na página impressa (o padrão).</span><span class="sxs-lookup"><span data-stu-id="34917-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34917-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="34917-111">Remarks</span></span>

<span data-ttu-id="34917-p101">Por padrão, as páginas de desenho são justificadas ao alto e à esquerda da página impressa. A configuração das células CenterX e CenterY como VERDADEIRO coloca a página de desenho no centro da página impressa (ou páginas quando for necessário colocar lado a lado).</span><span class="sxs-lookup"><span data-stu-id="34917-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="34917-114">Para fazer referência à célula CenterY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="34917-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34917-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="34917-115">Cell name:</span></span>  <br/> | <span data-ttu-id="34917-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="34917-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="34917-117">Para fazer referência à célula CenterY pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="34917-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34917-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="34917-118">Section index:</span></span>  <br/> |<span data-ttu-id="34917-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34917-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="34917-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="34917-120">Row index:</span></span>  <br/> |<span data-ttu-id="34917-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="34917-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="34917-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="34917-122">Cell index:</span></span>  <br/> |<span data-ttu-id="34917-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="34917-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

