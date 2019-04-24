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
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341913"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="83d02-103">Célula CenterY (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="83d02-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="83d02-104">Determina se a página de desenho ficará centralizada verticalmente na página impressa.</span><span class="sxs-lookup"><span data-stu-id="83d02-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="83d02-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="83d02-105">**Value**</span></span>|<span data-ttu-id="83d02-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="83d02-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="83d02-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="83d02-107">TRUE</span></span>  <br/> | <span data-ttu-id="83d02-108">Centraliza a página de desenho verticalmente na página impressa.</span><span class="sxs-lookup"><span data-stu-id="83d02-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="83d02-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="83d02-109">FALSE</span></span>  <br/> | <span data-ttu-id="83d02-110">Não centraliza a página de desenho verticalmente na página impressa (o padrão).</span><span class="sxs-lookup"><span data-stu-id="83d02-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83d02-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="83d02-111">Remarks</span></span>

<span data-ttu-id="83d02-p101">Por padrão, as páginas de desenho são justificadas ao alto e à esquerda da página impressa. A configuração das células CenterX e CenterY como VERDADEIRO coloca a página de desenho no centro da página impressa (ou páginas quando for necessário colocar lado a lado).</span><span class="sxs-lookup"><span data-stu-id="83d02-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="83d02-114">Para fazer referência à célula CenterY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="83d02-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83d02-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="83d02-115">Cell name:</span></span>  <br/> | <span data-ttu-id="83d02-116">Centro</span><span class="sxs-lookup"><span data-stu-id="83d02-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="83d02-117">Para fazer referência à célula CenterY pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="83d02-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83d02-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="83d02-118">Section index:</span></span>  <br/> |<span data-ttu-id="83d02-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="83d02-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="83d02-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="83d02-120">Row index:</span></span>  <br/> |<span data-ttu-id="83d02-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="83d02-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="83d02-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="83d02-122">Cell index:</span></span>  <br/> |<span data-ttu-id="83d02-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="83d02-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

