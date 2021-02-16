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
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413182"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="317ed-103">Célula DisplayMode (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="317ed-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="317ed-104">Determina como a forma do grupo e seus membros são exibidos.</span><span class="sxs-lookup"><span data-stu-id="317ed-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="317ed-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="317ed-105">**Value**</span></span>|<span data-ttu-id="317ed-106">**Modo de Exibição**</span><span class="sxs-lookup"><span data-stu-id="317ed-106">**Display Mode**</span></span>|<span data-ttu-id="317ed-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="317ed-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="317ed-108">0</span><span class="sxs-lookup"><span data-stu-id="317ed-108">0</span></span>  <br/> |<span data-ttu-id="317ed-109">Oculta o texto e a forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="317ed-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="317ed-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="317ed-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="317ed-111">1 </span><span class="sxs-lookup"><span data-stu-id="317ed-111">1</span></span>  <br/> |<span data-ttu-id="317ed-112">Exibe a forma do grupo atrás das formas dos membros.</span><span class="sxs-lookup"><span data-stu-id="317ed-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="317ed-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="317ed-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="317ed-114">2 </span><span class="sxs-lookup"><span data-stu-id="317ed-114">2</span></span>  <br/> |<span data-ttu-id="317ed-115">Exibe a forma do grupo na frente das formas dos membros.</span><span class="sxs-lookup"><span data-stu-id="317ed-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="317ed-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="317ed-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="317ed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="317ed-117">Remarks</span></span>

<span data-ttu-id="317ed-118">Você também pode definir esse valor selecionando o grupo, clicando em Comportamento no grupo **Design** da Forma na guia Desenvolvedor e selecionando um modo de exibição na lista de dados **do** grupo.  [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="317ed-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="317ed-119">Para obter uma referência para a célula DisplayMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="317ed-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="317ed-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="317ed-120">Cell name:</span></span>  <br/> |<span data-ttu-id="317ed-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="317ed-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="317ed-122">Para fazer referência à célula DisplayMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="317ed-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="317ed-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="317ed-123">Section index:</span></span>  <br/> |<span data-ttu-id="317ed-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="317ed-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="317ed-125">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="317ed-125">Row index:</span></span>  <br/> |<span data-ttu-id="317ed-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="317ed-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="317ed-127">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="317ed-127">Cell index:</span></span>  <br/> |<span data-ttu-id="317ed-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="317ed-128">**visGroupDisplayMode**</span></span> <br/> |
   

