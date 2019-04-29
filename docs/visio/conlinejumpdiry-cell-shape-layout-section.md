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
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404768"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="34e99-103">Célula ConLineJumpDirY (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="34e99-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="34e99-104">Determina a direção dos saltos de linha que ocorrem em um conector dinâmico vertical para uma forma.</span><span class="sxs-lookup"><span data-stu-id="34e99-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="34e99-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="34e99-105">**Value**</span></span>|<span data-ttu-id="34e99-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="34e99-106">**Line Jump Direction**</span></span>|<span data-ttu-id="34e99-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="34e99-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="34e99-108">,0</span><span class="sxs-lookup"><span data-stu-id="34e99-108">0</span></span>  <br/> | <span data-ttu-id="34e99-109">Padrão da página</span><span class="sxs-lookup"><span data-stu-id="34e99-109">Page default</span></span>  <br/> |<span data-ttu-id="34e99-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="34e99-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="34e99-111">1</span><span class="sxs-lookup"><span data-stu-id="34e99-111">1</span></span>  <br/> | <span data-ttu-id="34e99-112">Esquerdo</span><span class="sxs-lookup"><span data-stu-id="34e99-112">Left</span></span>  <br/> |<span data-ttu-id="34e99-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="34e99-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="34e99-114">duas</span><span class="sxs-lookup"><span data-stu-id="34e99-114">2</span></span>  <br/> | <span data-ttu-id="34e99-115">À direita</span><span class="sxs-lookup"><span data-stu-id="34e99-115">Right</span></span>  <br/> |<span data-ttu-id="34e99-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="34e99-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34e99-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="34e99-117">Remarks</span></span>

<span data-ttu-id="34e99-118">Para definir a direção vertical padrão para *todos os* saltos de conectores em uma página, use a célula PageLineJumpDirY na seção Page Layout.</span><span class="sxs-lookup"><span data-stu-id="34e99-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="34e99-119">Para fazer referência à célula ConLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="34e99-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34e99-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="34e99-120">Cell name:</span></span>  <br/> | <span data-ttu-id="34e99-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="34e99-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="34e99-122">Para fazer referência à célula ConLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="34e99-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34e99-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="34e99-123">Section index:</span></span>  <br/> |<span data-ttu-id="34e99-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34e99-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="34e99-125">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="34e99-125">Row index:</span></span>  <br/> |<span data-ttu-id="34e99-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="34e99-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="34e99-127">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="34e99-127">Cell index:</span></span>  <br/> |<span data-ttu-id="34e99-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="34e99-128">**visSLOJumpDirY**</span></span> <br/> |
   

