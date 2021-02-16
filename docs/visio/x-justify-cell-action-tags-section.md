---
title: Célula X Justify (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: O deslocamento x do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414120"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="169bf-103">Célula X Justify (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="169bf-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="169bf-104">O  *deslocamento x*  do botão de marca de ação em relação ao ponto definido pelas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="169bf-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="169bf-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="169bf-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="169bf-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="169bf-106">**Value**</span></span>|<span data-ttu-id="169bf-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="169bf-107">**Description**</span></span>|<span data-ttu-id="169bf-108">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="169bf-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="169bf-109">0</span><span class="sxs-lookup"><span data-stu-id="169bf-109">0</span></span>  <br/> | <span data-ttu-id="169bf-110">Justificado à esquerda (padrão).</span><span class="sxs-lookup"><span data-stu-id="169bf-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="169bf-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="169bf-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="169bf-112">1 </span><span class="sxs-lookup"><span data-stu-id="169bf-112">1</span></span>  <br/> | <span data-ttu-id="169bf-113">Centralizado.</span><span class="sxs-lookup"><span data-stu-id="169bf-113">Centered.</span></span>  <br/> |<span data-ttu-id="169bf-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="169bf-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="169bf-115">2 </span><span class="sxs-lookup"><span data-stu-id="169bf-115">2</span></span>  <br/> | <span data-ttu-id="169bf-116">Justificado à direita.</span><span class="sxs-lookup"><span data-stu-id="169bf-116">Right justified.</span></span>  <br/> |<span data-ttu-id="169bf-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="169bf-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="169bf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="169bf-118">Remarks</span></span>

<span data-ttu-id="169bf-119">As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="169bf-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="169bf-120">Para fazer referência à célula X Justify pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="169bf-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="169bf-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="169bf-121">Cell name:</span></span>  <br/> | <span data-ttu-id="169bf-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="169bf-122">SmartTags.</span></span>  <span data-ttu-id="169bf-123">*nome*  . XJustify onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="169bf-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="169bf-124">*nome*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="169bf-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="169bf-125">Para fazer referência à célula X Justify pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="169bf-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="169bf-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="169bf-126">Section index:</span></span>  <br/> |<span data-ttu-id="169bf-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="169bf-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="169bf-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="169bf-128">Row index:</span></span>  <br/> |<span data-ttu-id="169bf-129">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="169bf-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="169bf-130">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="169bf-130">Cell index:</span></span>  <br/> |<span data-ttu-id="169bf-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="169bf-131">**visSmartTagXJustify**</span></span> <br/> |
   

