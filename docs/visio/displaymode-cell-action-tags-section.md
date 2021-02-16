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
description: Determina se a marca de ação é exibida quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415814"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="9149f-103">Célula DisplayMode (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="9149f-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="9149f-104">Determina se a marca de ação é exibida quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.</span><span class="sxs-lookup"><span data-stu-id="9149f-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9149f-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="9149f-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="9149f-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9149f-106">**Value**</span></span>|<span data-ttu-id="9149f-107">**Modo de Exibição**</span><span class="sxs-lookup"><span data-stu-id="9149f-107">**Display Mode**</span></span>|<span data-ttu-id="9149f-108">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="9149f-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9149f-109">0</span><span class="sxs-lookup"><span data-stu-id="9149f-109">0</span></span>  <br/> | <span data-ttu-id="9149f-110">Aparece quando o mouse é pausado sobre a marca (o padrão).</span><span class="sxs-lookup"><span data-stu-id="9149f-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="9149f-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="9149f-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="9149f-112">1 </span><span class="sxs-lookup"><span data-stu-id="9149f-112">1</span></span>  <br/> | <span data-ttu-id="9149f-113">Exibido enquanto a forma é selecionada.</span><span class="sxs-lookup"><span data-stu-id="9149f-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="9149f-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="9149f-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="9149f-115">2 </span><span class="sxs-lookup"><span data-stu-id="9149f-115">2</span></span>  <br/> | <span data-ttu-id="9149f-116">Sempre exibido.</span><span class="sxs-lookup"><span data-stu-id="9149f-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="9149f-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="9149f-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9149f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9149f-118">Remarks</span></span>

<span data-ttu-id="9149f-119">As marcas de ação não aparecem no material impresso nem publicado.</span><span class="sxs-lookup"><span data-stu-id="9149f-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="9149f-120">Se uma marca de ação for definida para uma página e essa célula contiver o valor 1, a marca nunca será exibida pois a página não pode ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="9149f-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="9149f-121">Para fazer referência à célula DisplayMode pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9149f-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9149f-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9149f-122">Cell name:</span></span>  <br/> | <span data-ttu-id="9149f-123">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9149f-123">SmartTags.</span></span>  <span data-ttu-id="9149f-124">*nome*  . DisplayMode onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9149f-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="9149f-125">*nome*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="9149f-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="9149f-126">Para fazer referência à célula DisplayMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9149f-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9149f-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9149f-127">Section index:</span></span>  <br/> |<span data-ttu-id="9149f-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="9149f-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="9149f-129">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="9149f-129">Row index:</span></span>  <br/> |<span data-ttu-id="9149f-130">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9149f-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9149f-131">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="9149f-131">Cell index:</span></span>  <br/> |<span data-ttu-id="9149f-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="9149f-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

