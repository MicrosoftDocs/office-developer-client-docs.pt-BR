---
title: Célula PageLineJumpDirX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Determina a direção dos saltos de linha em conectores dinâmicos horizontais na página de desenho para a qual uma direção de salto local não foi aplicada.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772453"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="4dc0f-103">Célula LineJumpDirX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="4dc0f-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="4dc0f-104">Determina a direção dos saltos de linha em conectores dinâmicos horizontais na página de desenho para a qual uma direção de salto local não foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="4dc0f-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="4dc0f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-105">**Value**</span></span>|<span data-ttu-id="4dc0f-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-106">**Line jump direction**</span></span>|<span data-ttu-id="4dc0f-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4dc0f-108">0</span><span class="sxs-lookup"><span data-stu-id="4dc0f-108">0</span></span>  <br/> | <span data-ttu-id="4dc0f-109">Padrão; à esquerda ou a definição da página para formas</span><span class="sxs-lookup"><span data-stu-id="4dc0f-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="4dc0f-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="4dc0f-111">1</span><span class="sxs-lookup"><span data-stu-id="4dc0f-111">1</span></span>  <br/> | <span data-ttu-id="4dc0f-112">Acima</span><span class="sxs-lookup"><span data-stu-id="4dc0f-112">Up</span></span>  <br/> |<span data-ttu-id="4dc0f-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="4dc0f-114">2</span><span class="sxs-lookup"><span data-stu-id="4dc0f-114">2</span></span>  <br/> | <span data-ttu-id="4dc0f-115">Abaixo</span><span class="sxs-lookup"><span data-stu-id="4dc0f-115">Down</span></span>  <br/> |<span data-ttu-id="4dc0f-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dc0f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dc0f-117">Remarks</span></span>

<span data-ttu-id="4dc0f-118">Para fazer referência à célula PageLineJumpDirX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4dc0f-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4dc0f-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4dc0f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="4dc0f-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="4dc0f-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="4dc0f-121">Para fazer referência à célula PageLineJumpDirX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4dc0f-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4dc0f-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4dc0f-122">Section index:</span></span>  <br/> |<span data-ttu-id="4dc0f-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4dc0f-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4dc0f-124">Row index:</span></span>  <br/> |<span data-ttu-id="4dc0f-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="4dc0f-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4dc0f-126">Cell index:</span></span>  <br/> |<span data-ttu-id="4dc0f-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="4dc0f-127">**visPLOJumpDirX**</span></span> <br/> |
   

