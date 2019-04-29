---
title: Célula ReplaceLockFormat (seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. Se a célula ReplaceLockFormat de uma forma mestre for definida como TRUE (1), os valores de formatação do mestre substituirão todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427231"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="8e6d3-104">Célula ReplaceLockFormat (seção Change Shape Behavior)</span><span class="sxs-lookup"><span data-stu-id="8e6d3-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="8e6d3-105">Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="8e6d3-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="8e6d3-106">Se a célula **ReplaceLockFormat** de uma forma mestre for definida como true (1), os valores de formatação do mestre substituirão todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.</span><span class="sxs-lookup"><span data-stu-id="8e6d3-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="8e6d3-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-107">**Value**</span></span>|<span data-ttu-id="8e6d3-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e6d3-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="8e6d3-109">TRUE</span></span>  <br/> |<span data-ttu-id="8e6d3-110">Se a célula **ReplaceLockFormat** de uma forma mestre for definida como true, os valores de formatação do mestre substituirão todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.</span><span class="sxs-lookup"><span data-stu-id="8e6d3-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="8e6d3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8e6d3-111">FALSE</span></span>  <br/> |<span data-ttu-id="8e6d3-112">Se a célula **ReplaceLockFormat** de uma forma mestre estiver definida como false, a forma de substituição conterá os valores de formatação local da forma antiga após a operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="8e6d3-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e6d3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e6d3-113">Remarks</span></span>

<span data-ttu-id="8e6d3-114">A célula **ReplaceLockFormat** determina se a forma mestre substituirá os valores de formatação local das células nas seções a seguir durante uma operação de substituição de forma:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="8e6d3-115">Seção **Fill Format**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="8e6d3-116">Seção **line Format**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="8e6d3-117">Seção **Style rápido**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="8e6d3-118">Seção **Theme Properties**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="8e6d3-119">Seção **Propriedades** de gradiente</span><span class="sxs-lookup"><span data-stu-id="8e6d3-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="8e6d3-120">Seção de **Propriedades de bisel**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="8e6d3-121">Seção **Additional Effect Properties**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="8e6d3-122">Seção paradas de gradiente de **linha**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="8e6d3-123">Seção **Fill gradientout**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="8e6d3-124">Para obter uma referência para a célula **ReplaceLockFormat** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e6d3-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-125">Cell name:</span></span>  <br/> | <span data-ttu-id="8e6d3-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="8e6d3-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="8e6d3-127">Para obter uma referência para a célula **ReplaceLockFormat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e6d3-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-128">Section index:</span></span>  <br/> |<span data-ttu-id="8e6d3-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8e6d3-130">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-130">Row index:</span></span>  <br/> |<span data-ttu-id="8e6d3-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="8e6d3-132">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8e6d3-132">Cell index:</span></span>  <br/> |<span data-ttu-id="8e6d3-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="8e6d3-133">**visReplaceLockFormat**</span></span> <br/> |
   

