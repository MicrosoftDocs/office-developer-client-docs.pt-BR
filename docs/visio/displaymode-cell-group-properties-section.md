---
title: Célula DisplayMode (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Determina como a forma do grupo e seus membros são exibidos.
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771723"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="e0537-103">Célula DisplayMode (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="e0537-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="e0537-104">Determina como a forma do grupo e seus membros são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e0537-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="e0537-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e0537-105">**Value**</span></span>|<span data-ttu-id="e0537-106">**Modo de exibição**</span><span class="sxs-lookup"><span data-stu-id="e0537-106">**Display Mode**</span></span>|<span data-ttu-id="e0537-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e0537-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0537-108">0</span><span class="sxs-lookup"><span data-stu-id="e0537-108">0</span></span>  <br/> |<span data-ttu-id="e0537-109">Oculta o texto e a forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="e0537-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="e0537-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="e0537-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="e0537-111">1</span><span class="sxs-lookup"><span data-stu-id="e0537-111">1</span></span>  <br/> |<span data-ttu-id="e0537-112">Exibe a forma do grupo atrás das formas dos membros.</span><span class="sxs-lookup"><span data-stu-id="e0537-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="e0537-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="e0537-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="e0537-114">2</span><span class="sxs-lookup"><span data-stu-id="e0537-114">2</span></span>  <br/> |<span data-ttu-id="e0537-115">Exibe a forma do grupo na frente das formas dos membros.</span><span class="sxs-lookup"><span data-stu-id="e0537-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="e0537-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="e0537-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0537-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0537-117">Remarks</span></span>

<span data-ttu-id="e0537-118">Você pode também definir esse valor selecionando o grupo, clicando em **comportamento** , no grupo **Design** da forma na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, selecionando um modo de exibição da lista de **dados de grupo** .</span><span class="sxs-lookup"><span data-stu-id="e0537-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="e0537-119">Para obter uma referência para a célula DisplayMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e0537-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0537-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e0537-120">Cell name:</span></span>  <br/> |<span data-ttu-id="e0537-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="e0537-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="e0537-122">Para obter uma referência para a célula DisplayMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e0537-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0537-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e0537-123">Section index:</span></span>  <br/> |<span data-ttu-id="e0537-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e0537-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e0537-125">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e0537-125">Row index:</span></span>  <br/> |<span data-ttu-id="e0537-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="e0537-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="e0537-127">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e0537-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e0537-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="e0537-128">**visGroupDisplayMode**</span></span> <br/> |
   

