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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419979"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="7045a-103">Célula Y Justify (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="7045a-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="7045a-104">O  *deslocamento y*  do botão de marca de ação em relação ao ponto definido pelas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="7045a-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7045a-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="7045a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7045a-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7045a-106">**Value**</span></span>|<span data-ttu-id="7045a-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7045a-107">**Description**</span></span>|<span data-ttu-id="7045a-108">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="7045a-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7045a-109">0</span><span class="sxs-lookup"><span data-stu-id="7045a-109">0</span></span>  <br/> | <span data-ttu-id="7045a-110">Justificado no topo (padrão).</span><span class="sxs-lookup"><span data-stu-id="7045a-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="7045a-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="7045a-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="7045a-112">1 </span><span class="sxs-lookup"><span data-stu-id="7045a-112">1</span></span>  <br/> | <span data-ttu-id="7045a-113">Centralizado.</span><span class="sxs-lookup"><span data-stu-id="7045a-113">Centered.</span></span>  <br/> |<span data-ttu-id="7045a-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="7045a-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="7045a-115">2 </span><span class="sxs-lookup"><span data-stu-id="7045a-115">2</span></span>  <br/> | <span data-ttu-id="7045a-116">Justificado na base.</span><span class="sxs-lookup"><span data-stu-id="7045a-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="7045a-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="7045a-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7045a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7045a-118">Remarks</span></span>

<span data-ttu-id="7045a-119">As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="7045a-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="7045a-120">Para fazer referência à célula Y Justify pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7045a-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7045a-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7045a-121">Cell name:</span></span>  <br/> | <span data-ttu-id="7045a-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="7045a-122">SmartTags.</span></span>  <span data-ttu-id="7045a-123">*nome*  . YJustify onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="7045a-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="7045a-124">*nome*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="7045a-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="7045a-125">Para fazer referência à célula X Justify pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7045a-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7045a-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7045a-126">Section index:</span></span>  <br/> |<span data-ttu-id="7045a-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="7045a-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="7045a-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="7045a-128">Row index:</span></span>  <br/> |<span data-ttu-id="7045a-129">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7045a-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7045a-130">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="7045a-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7045a-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="7045a-131">**visSmartTagYJustify**</span></span> <br/> |
   

