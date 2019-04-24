---
title: Célula PageLineJumpDirY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Determina a direção dos saltos de linha em conectores dinâmicos verticais na página de desenho para a qual uma direção de salto local não foi aplicada.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329894"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="1bb31-103">Célula PageLineJumpDirY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="1bb31-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="1bb31-104">Determina a direção dos saltos de linha em conectores dinâmicos verticais na página de desenho para a qual uma direção de salto local não foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="1bb31-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="1bb31-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1bb31-105">**Value**</span></span>|<span data-ttu-id="1bb31-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="1bb31-106">**Line jump direction**</span></span>|<span data-ttu-id="1bb31-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="1bb31-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1bb31-108">,0</span><span class="sxs-lookup"><span data-stu-id="1bb31-108">0</span></span>  <br/> | <span data-ttu-id="1bb31-109">Padrão; acima ou a definição da página para formas</span><span class="sxs-lookup"><span data-stu-id="1bb31-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="1bb31-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="1bb31-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="1bb31-111">1</span><span class="sxs-lookup"><span data-stu-id="1bb31-111">1</span></span>  <br/> | <span data-ttu-id="1bb31-112">Esquerdo</span><span class="sxs-lookup"><span data-stu-id="1bb31-112">Left</span></span>  <br/> |<span data-ttu-id="1bb31-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="1bb31-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="1bb31-114">duas</span><span class="sxs-lookup"><span data-stu-id="1bb31-114">2</span></span>  <br/> | <span data-ttu-id="1bb31-115">À direita</span><span class="sxs-lookup"><span data-stu-id="1bb31-115">Right</span></span>  <br/> |<span data-ttu-id="1bb31-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="1bb31-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bb31-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bb31-117">Remarks</span></span>

<span data-ttu-id="1bb31-118">Para fazer referência à célula PageLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="1bb31-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1bb31-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1bb31-119">Cell name:</span></span>  <br/> | <span data-ttu-id="1bb31-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="1bb31-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="1bb31-121">Para fazer referência à célula PageLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1bb31-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1bb31-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1bb31-122">Section index:</span></span>  <br/> |<span data-ttu-id="1bb31-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1bb31-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1bb31-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1bb31-124">Row index:</span></span>  <br/> |<span data-ttu-id="1bb31-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1bb31-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="1bb31-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1bb31-126">Cell index:</span></span>  <br/> |<span data-ttu-id="1bb31-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="1bb31-127">**visPLOJumpDirY**</span></span> <br/> |
   

