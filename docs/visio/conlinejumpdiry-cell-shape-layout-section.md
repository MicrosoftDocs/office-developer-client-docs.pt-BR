---
title: Célula ConLineJumpDirY (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Determina a direção dos saltos de linha que ocorrem em um conector dinâmico vertical para uma forma.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771561"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="f849e-103">Célula ConLineJumpDirY (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="f849e-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="f849e-104">Determina a direção dos saltos de linha que ocorrem em um conector dinâmico vertical para uma forma.</span><span class="sxs-lookup"><span data-stu-id="f849e-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="f849e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f849e-105">**Value**</span></span>|<span data-ttu-id="f849e-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="f849e-106">**Line Jump Direction**</span></span>|<span data-ttu-id="f849e-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="f849e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f849e-108">0</span><span class="sxs-lookup"><span data-stu-id="f849e-108">0</span></span>  <br/> | <span data-ttu-id="f849e-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="f849e-109">Page default</span></span>  <br/> |<span data-ttu-id="f849e-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="f849e-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="f849e-111">1</span><span class="sxs-lookup"><span data-stu-id="f849e-111">1</span></span>  <br/> | <span data-ttu-id="f849e-112">Esquerda</span><span class="sxs-lookup"><span data-stu-id="f849e-112">Left</span></span>  <br/> |<span data-ttu-id="f849e-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="f849e-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="f849e-114">2</span><span class="sxs-lookup"><span data-stu-id="f849e-114">2</span></span>  <br/> | <span data-ttu-id="f849e-115">Direita</span><span class="sxs-lookup"><span data-stu-id="f849e-115">Right</span></span>  <br/> |<span data-ttu-id="f849e-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="f849e-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f849e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f849e-117">Remarks</span></span>

<span data-ttu-id="f849e-118">Para definir o padrão direção vertical para *todos os* conector salta em uma página, utilize a célula PageLineJumpDirY na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="f849e-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="f849e-119">Para fazer referência à célula ConLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f849e-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f849e-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f849e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="f849e-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="f849e-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="f849e-122">Para fazer referência à célula ConLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f849e-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f849e-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f849e-123">Section index:</span></span>  <br/> |<span data-ttu-id="f849e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f849e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f849e-125">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f849e-125">Row index:</span></span>  <br/> |<span data-ttu-id="f849e-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="f849e-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="f849e-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f849e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="f849e-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="f849e-128">**visSLOJumpDirY**</span></span> <br/> |
   

