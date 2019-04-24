---
title: Célula Y Justify (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: O deslocamento y do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357012"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="3ed64-103">Célula Y Justify (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="3ed64-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="3ed64-104">O deslocamento *y* do botão de marca de ação em relação ao ponto definido pelas células X e y.</span><span class="sxs-lookup"><span data-stu-id="3ed64-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3ed64-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="3ed64-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="3ed64-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3ed64-106">**Value**</span></span>|<span data-ttu-id="3ed64-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ed64-107">**Description**</span></span>|<span data-ttu-id="3ed64-108">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="3ed64-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3ed64-109">,0</span><span class="sxs-lookup"><span data-stu-id="3ed64-109">0</span></span>  <br/> | <span data-ttu-id="3ed64-110">Justificado no topo (padrão).</span><span class="sxs-lookup"><span data-stu-id="3ed64-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="3ed64-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="3ed64-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="3ed64-112">1</span><span class="sxs-lookup"><span data-stu-id="3ed64-112">1</span></span>  <br/> | <span data-ttu-id="3ed64-113">Centralizado.</span><span class="sxs-lookup"><span data-stu-id="3ed64-113">Centered.</span></span>  <br/> |<span data-ttu-id="3ed64-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="3ed64-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="3ed64-115">duas</span><span class="sxs-lookup"><span data-stu-id="3ed64-115">2</span></span>  <br/> | <span data-ttu-id="3ed64-116">Justificado na base.</span><span class="sxs-lookup"><span data-stu-id="3ed64-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="3ed64-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="3ed64-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ed64-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ed64-118">Remarks</span></span>

<span data-ttu-id="3ed64-119">As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="3ed64-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="3ed64-120">Para fazer referência à célula Y Justify pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3ed64-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ed64-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3ed64-121">Cell name:</span></span>  <br/> | <span data-ttu-id="3ed64-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3ed64-122">SmartTags.</span></span>  <span data-ttu-id="3ed64-123">*nome* . YJustify onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3ed64-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="3ed64-124">*name*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="3ed64-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3ed64-125">Para fazer referência à célula X Justify pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3ed64-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ed64-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3ed64-126">Section index:</span></span>  <br/> |<span data-ttu-id="3ed64-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3ed64-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3ed64-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3ed64-128">Row index:</span></span>  <br/> |<span data-ttu-id="3ed64-129">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ed64-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3ed64-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3ed64-130">Cell index:</span></span>  <br/> |<span data-ttu-id="3ed64-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="3ed64-131">**visSmartTagYJustify**</span></span> <br/> |
   

