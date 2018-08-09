---
title: Célula DisplayMode (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Determina se a marca de ação aparece quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771711"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="657fe-103">Célula DisplayMode (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="657fe-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="657fe-104">Determina se a marca de ação aparece quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.</span><span class="sxs-lookup"><span data-stu-id="657fe-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="657fe-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="657fe-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="657fe-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="657fe-106">**Value**</span></span>|<span data-ttu-id="657fe-107">**Modo de exibição**</span><span class="sxs-lookup"><span data-stu-id="657fe-107">**Display Mode**</span></span>|<span data-ttu-id="657fe-108">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="657fe-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="657fe-109">0</span><span class="sxs-lookup"><span data-stu-id="657fe-109">0</span></span>  <br/> | <span data-ttu-id="657fe-110">Aparece quando o mouse é pausado sobre a marca (padrão).</span><span class="sxs-lookup"><span data-stu-id="657fe-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="657fe-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="657fe-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="657fe-112">1</span><span class="sxs-lookup"><span data-stu-id="657fe-112">1</span></span>  <br/> | <span data-ttu-id="657fe-113">Exibido enquanto a forma é selecionada.</span><span class="sxs-lookup"><span data-stu-id="657fe-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="657fe-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="657fe-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="657fe-115">2</span><span class="sxs-lookup"><span data-stu-id="657fe-115">2</span></span>  <br/> | <span data-ttu-id="657fe-116">Sempre exibido.</span><span class="sxs-lookup"><span data-stu-id="657fe-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="657fe-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="657fe-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="657fe-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="657fe-118">Remarks</span></span>

<span data-ttu-id="657fe-119">As marcas de ação não aparecem no material impresso nem publicado.</span><span class="sxs-lookup"><span data-stu-id="657fe-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="657fe-120">Se uma marca de ação for definida para uma página e essa célula contiver o valor 1, a marca nunca será exibida pois a página não pode ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="657fe-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="657fe-121">Para fazer referência à célula DisplayMode pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="657fe-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="657fe-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="657fe-122">Cell name:</span></span>  <br/> | <span data-ttu-id="657fe-123">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="657fe-123">SmartTags.</span></span>  <span data-ttu-id="657fe-124">*nome* . DisplayMode onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="657fe-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="657fe-125">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="657fe-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="657fe-126">Para obter uma referência para a célula DisplayMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="657fe-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="657fe-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="657fe-127">Section index:</span></span>  <br/> |<span data-ttu-id="657fe-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="657fe-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="657fe-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="657fe-129">Row index:</span></span>  <br/> |<span data-ttu-id="657fe-130">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="657fe-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="657fe-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="657fe-131">Cell index:</span></span>  <br/> |<span data-ttu-id="657fe-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="657fe-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

