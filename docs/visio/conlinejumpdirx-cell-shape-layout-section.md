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
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771573"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="10fbc-103">Célula ConLineJumpDirX (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="10fbc-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="10fbc-104">Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.</span><span class="sxs-lookup"><span data-stu-id="10fbc-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="10fbc-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="10fbc-105">**Value**</span></span>|<span data-ttu-id="10fbc-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="10fbc-106">**Line jump direction**</span></span>|<span data-ttu-id="10fbc-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="10fbc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="10fbc-108">0</span><span class="sxs-lookup"><span data-stu-id="10fbc-108">0</span></span>  <br/> | <span data-ttu-id="10fbc-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="10fbc-109">Page default</span></span>  <br/> |<span data-ttu-id="10fbc-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="10fbc-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="10fbc-111">1</span><span class="sxs-lookup"><span data-stu-id="10fbc-111">1</span></span>  <br/> | <span data-ttu-id="10fbc-112">Acima</span><span class="sxs-lookup"><span data-stu-id="10fbc-112">Up</span></span>  <br/> |<span data-ttu-id="10fbc-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="10fbc-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="10fbc-114">2</span><span class="sxs-lookup"><span data-stu-id="10fbc-114">2</span></span>  <br/> | <span data-ttu-id="10fbc-115">Abaixo</span><span class="sxs-lookup"><span data-stu-id="10fbc-115">Down</span></span>  <br/> |<span data-ttu-id="10fbc-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="10fbc-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10fbc-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="10fbc-117">Remarks</span></span>

<span data-ttu-id="10fbc-118">Para definir o padrão direção horizontal para o conector de *todos os* saltos em uma página, utilize a célula PageLineJumpDirX na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="10fbc-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="10fbc-119">Para obter uma referência à célula ConLineJumpDirX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="10fbc-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10fbc-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="10fbc-120">Cell name:</span></span>  <br/> | <span data-ttu-id="10fbc-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="10fbc-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="10fbc-122">Para obter uma referência à célula ConLineJumpDirX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="10fbc-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10fbc-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="10fbc-123">Section index:</span></span>  <br/> |<span data-ttu-id="10fbc-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10fbc-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="10fbc-125">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="10fbc-125">Row index:</span></span>  <br/> |<span data-ttu-id="10fbc-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="10fbc-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="10fbc-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="10fbc-127">Cell index:</span></span>  <br/> |<span data-ttu-id="10fbc-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="10fbc-128">**visSLOJumpDirX**</span></span> <br/> |
   

