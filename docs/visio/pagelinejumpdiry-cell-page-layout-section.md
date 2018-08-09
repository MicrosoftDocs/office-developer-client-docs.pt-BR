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
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772464"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="0a491-103">Célula LineJumpDirY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="0a491-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="0a491-104">Determina a direção dos saltos de linha em conectores dinâmicos verticais na página de desenho para a qual uma direção de salto local não foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="0a491-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="0a491-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0a491-105">**Value**</span></span>|<span data-ttu-id="0a491-106">**Direção do salto de linha**</span><span class="sxs-lookup"><span data-stu-id="0a491-106">**Line jump direction**</span></span>|<span data-ttu-id="0a491-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="0a491-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0a491-108">0</span><span class="sxs-lookup"><span data-stu-id="0a491-108">0</span></span>  <br/> | <span data-ttu-id="0a491-109">Padrão; acima ou a definição da página para formas</span><span class="sxs-lookup"><span data-stu-id="0a491-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="0a491-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="0a491-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="0a491-111">1</span><span class="sxs-lookup"><span data-stu-id="0a491-111">1</span></span>  <br/> | <span data-ttu-id="0a491-112">Esquerda</span><span class="sxs-lookup"><span data-stu-id="0a491-112">Left</span></span>  <br/> |<span data-ttu-id="0a491-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="0a491-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="0a491-114">2</span><span class="sxs-lookup"><span data-stu-id="0a491-114">2</span></span>  <br/> | <span data-ttu-id="0a491-115">Direita</span><span class="sxs-lookup"><span data-stu-id="0a491-115">Right</span></span>  <br/> |<span data-ttu-id="0a491-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="0a491-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a491-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a491-117">Remarks</span></span>

<span data-ttu-id="0a491-118">Para fazer referência à célula PageLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0a491-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a491-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0a491-119">Cell name:</span></span>  <br/> | <span data-ttu-id="0a491-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="0a491-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="0a491-121">Para fazer referência à célula PageLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0a491-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a491-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0a491-122">Section index:</span></span>  <br/> |<span data-ttu-id="0a491-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a491-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0a491-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0a491-124">Row index:</span></span>  <br/> |<span data-ttu-id="0a491-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0a491-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="0a491-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0a491-126">Cell index:</span></span>  <br/> |<span data-ttu-id="0a491-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="0a491-127">**visPLOJumpDirY**</span></span> <br/> |
   

