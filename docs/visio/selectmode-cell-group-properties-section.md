---
title: Célula SelectMode (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Determina como selecionar uma forma de grupo e seus membros.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435359"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="4d8d3-103">Célula SelectMode (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="4d8d3-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="4d8d3-104">Determina como selecionar uma forma de grupo e seus membros.</span><span class="sxs-lookup"><span data-stu-id="4d8d3-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="4d8d3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-105">**Value**</span></span>|<span data-ttu-id="4d8d3-106">**Modo de seleção**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-106">**Selection mode**</span></span>|<span data-ttu-id="4d8d3-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d8d3-108">0</span><span class="sxs-lookup"><span data-stu-id="4d8d3-108">0</span></span>  <br/> |<span data-ttu-id="4d8d3-109">Selecionar somente a forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d8d3-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="4d8d3-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="4d8d3-111">1 </span><span class="sxs-lookup"><span data-stu-id="4d8d3-111">1</span></span>  <br/> |<span data-ttu-id="4d8d3-112">Selecionar primeiro a forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d8d3-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="4d8d3-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="4d8d3-114">2 </span><span class="sxs-lookup"><span data-stu-id="4d8d3-114">2</span></span>  <br/> |<span data-ttu-id="4d8d3-115">Selecionar primeiro os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="4d8d3-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="4d8d3-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d8d3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d8d3-117">Remarks</span></span>

<span data-ttu-id="4d8d3-118">Você também pode definir esse valor na caixa de diálogo Comportamento (com a forma de grupo selecionada, na guia  Desenvolvedor, no grupo **Design** da Forma, clique em Comportamento e em um modo na lista Seleção em Comportamento do **Grupo).**  [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="4d8d3-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="4d8d3-119">Para obter uma referência para a célula SelectMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4d8d3-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d8d3-120">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4d8d3-120">Cell name:</span></span>  <br/> |<span data-ttu-id="4d8d3-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="4d8d3-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="4d8d3-122">Para obter uma referência para a célula SelectMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4d8d3-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d8d3-123">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4d8d3-123">Section index:</span></span>  <br/> |<span data-ttu-id="4d8d3-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4d8d3-125">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="4d8d3-125">Row index:</span></span>  <br/> |<span data-ttu-id="4d8d3-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="4d8d3-127">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="4d8d3-127">Cell index:</span></span>  <br/> |<span data-ttu-id="4d8d3-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="4d8d3-128">**visGroupSelectMode**</span></span> <br/> |
   

