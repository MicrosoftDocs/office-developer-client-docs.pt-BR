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
description: O - deslocamento x do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773304"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="a68e6-103">Célula X Justify (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="a68e6-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="a68e6-104">*X* -deslocamento do botão de marca de ação em relação ao ponto definido pelas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="a68e6-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a68e6-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="a68e6-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="a68e6-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a68e6-106">**Value**</span></span>|<span data-ttu-id="a68e6-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a68e6-107">**Description**</span></span>|<span data-ttu-id="a68e6-108">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="a68e6-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a68e6-109">0</span><span class="sxs-lookup"><span data-stu-id="a68e6-109">0</span></span>  <br/> | <span data-ttu-id="a68e6-110">Justificado à esquerda (padrão).</span><span class="sxs-lookup"><span data-stu-id="a68e6-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="a68e6-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="a68e6-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="a68e6-112">1</span><span class="sxs-lookup"><span data-stu-id="a68e6-112">1</span></span>  <br/> | <span data-ttu-id="a68e6-113">Centralizado.</span><span class="sxs-lookup"><span data-stu-id="a68e6-113">Centered.</span></span>  <br/> |<span data-ttu-id="a68e6-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="a68e6-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="a68e6-115">2</span><span class="sxs-lookup"><span data-stu-id="a68e6-115">2</span></span>  <br/> | <span data-ttu-id="a68e6-116">Justificado à direita.</span><span class="sxs-lookup"><span data-stu-id="a68e6-116">Right justified.</span></span>  <br/> |<span data-ttu-id="a68e6-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="a68e6-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a68e6-118">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a68e6-118">Remarks</span></span>

<span data-ttu-id="a68e6-119">As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y.</span><span class="sxs-lookup"><span data-stu-id="a68e6-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="a68e6-120">Para fazer referência à célula X Justify pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="a68e6-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a68e6-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a68e6-121">Cell name:</span></span>  <br/> | <span data-ttu-id="a68e6-122">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="a68e6-122">SmartTags.</span></span>  <span data-ttu-id="a68e6-123">*nome* . XJustify onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="a68e6-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="a68e6-124">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="a68e6-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="a68e6-125">Para obter uma referência à célula X Justify pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a68e6-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a68e6-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a68e6-126">Section index:</span></span>  <br/> |<span data-ttu-id="a68e6-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="a68e6-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="a68e6-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a68e6-128">Row index:</span></span>  <br/> |<span data-ttu-id="a68e6-129">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a68e6-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a68e6-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a68e6-130">Cell index:</span></span>  <br/> |<span data-ttu-id="a68e6-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="a68e6-131">**visSmartTagXJustify**</span></span> <br/> |
   

