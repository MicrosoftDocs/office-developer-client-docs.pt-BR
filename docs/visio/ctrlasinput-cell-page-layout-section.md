---
title: Célula CtrlAsInput (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Determina a forma pai ao utilizar formas com alças de controle. Esta célula determina o comportamento de todas as formas na página de desenho.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282905"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="776e7-104">Célula CtrlAsInput (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="776e7-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="776e7-p102">Determina a forma pai ao utilizar formas com alças de controle. Esta célula determina o comportamento de todas as formas na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="776e7-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="776e7-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="776e7-107">**Value**</span></span>|<span data-ttu-id="776e7-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="776e7-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="776e7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="776e7-109">TRUE</span></span>  <br/> | <span data-ttu-id="776e7-110">Define como pai a forma à qual a alça de controle está conectada.</span><span class="sxs-lookup"><span data-stu-id="776e7-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="776e7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="776e7-111">FALSE</span></span>  <br/> | <span data-ttu-id="776e7-p103">O padrão. Define como pai a forma que contém a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="776e7-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="776e7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="776e7-114">Remarks</span></span>

<span data-ttu-id="776e7-115">Para fazer referência à célula CtrlAsInput pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="776e7-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="776e7-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="776e7-116">Cell name:</span></span>  <br/> | <span data-ttu-id="776e7-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="776e7-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="776e7-118">Para fazer referência à célula CtrlAsInput pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="776e7-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="776e7-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="776e7-119">Section index:</span></span>  <br/> |<span data-ttu-id="776e7-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="776e7-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="776e7-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="776e7-121">Row index:</span></span>  <br/> |<span data-ttu-id="776e7-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="776e7-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="776e7-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="776e7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="776e7-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="776e7-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

