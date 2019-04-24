---
title: Célula ConLineJumpDirX (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342746"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="7475e-103">Célula ConLineJumpDirX (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="7475e-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="7475e-104">Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.</span><span class="sxs-lookup"><span data-stu-id="7475e-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="7475e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7475e-105">**Value**</span></span>|<span data-ttu-id="7475e-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="7475e-106">**Line jump direction**</span></span>|<span data-ttu-id="7475e-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="7475e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7475e-108">,0</span><span class="sxs-lookup"><span data-stu-id="7475e-108">0</span></span>  <br/> | <span data-ttu-id="7475e-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="7475e-109">Page default</span></span>  <br/> |<span data-ttu-id="7475e-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="7475e-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="7475e-111">1</span><span class="sxs-lookup"><span data-stu-id="7475e-111">1</span></span>  <br/> | <span data-ttu-id="7475e-112">Para cima</span><span class="sxs-lookup"><span data-stu-id="7475e-112">Up</span></span>  <br/> |<span data-ttu-id="7475e-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="7475e-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="7475e-114">duas</span><span class="sxs-lookup"><span data-stu-id="7475e-114">2</span></span>  <br/> | <span data-ttu-id="7475e-115">Para baixo</span><span class="sxs-lookup"><span data-stu-id="7475e-115">Down</span></span>  <br/> |<span data-ttu-id="7475e-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="7475e-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7475e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7475e-117">Remarks</span></span>

<span data-ttu-id="7475e-118">Para definir a direção horizontal padrão para *todos os* saltos de conectores em uma página, use a célula PageLineJumpDirX na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="7475e-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="7475e-119">Para fazer referência à célula ConLineJumpDirX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7475e-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7475e-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7475e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="7475e-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="7475e-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="7475e-122">Para fazer referência à célula ConLineJumpDirX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7475e-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7475e-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7475e-123">Section index:</span></span>  <br/> |<span data-ttu-id="7475e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7475e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7475e-125">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7475e-125">Row index:</span></span>  <br/> |<span data-ttu-id="7475e-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="7475e-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="7475e-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7475e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="7475e-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="7475e-128">**visSLOJumpDirX**</span></span> <br/> |
   

