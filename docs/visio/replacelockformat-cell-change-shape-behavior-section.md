---
title: Célula ReplaceLockFormat (seção de comportamento de forma alterar)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. Se a célula ReplaceLockFormat de uma forma mestra é definida como verdadeiro (1), os valores de formatação do mestre substituir todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772694"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="05515-104">Célula ReplaceLockFormat (seção de comportamento de forma alterar)</span><span class="sxs-lookup"><span data-stu-id="05515-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="05515-105">Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="05515-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="05515-106">Se a célula **ReplaceLockFormat** de uma forma mestra é definida como verdadeiro (1), os valores de formatação do mestre substituir todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.</span><span class="sxs-lookup"><span data-stu-id="05515-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="05515-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="05515-107">**Value**</span></span>|<span data-ttu-id="05515-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="05515-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05515-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="05515-109">TRUE</span></span>  <br/> |<span data-ttu-id="05515-110">Se a célula **ReplaceLockFormat** de uma forma mestra for definida como TRUE, os valores de formatação do mestre substituir todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.</span><span class="sxs-lookup"><span data-stu-id="05515-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="05515-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="05515-111">FALSE</span></span>  <br/> |<span data-ttu-id="05515-112">Se a célula **ReplaceLockFormat** de uma forma mestra for definida como FALSE, a forma de substituição contém os valores de formatação locais da forma antigo após a operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="05515-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05515-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="05515-113">Remarks</span></span>

<span data-ttu-id="05515-114">A célula **ReplaceLockFormat** determina se a forma mestra substitui os valores de formatação locais das células nas seções a seguir durante uma operação de substituição de forma:</span><span class="sxs-lookup"><span data-stu-id="05515-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="05515-115">Seção **Fill Format**</span><span class="sxs-lookup"><span data-stu-id="05515-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="05515-116">Seção **Line Format**</span><span class="sxs-lookup"><span data-stu-id="05515-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="05515-117">Seção de **Estilos Rápidos**</span><span class="sxs-lookup"><span data-stu-id="05515-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="05515-118">Seção de **Propriedades do tema**</span><span class="sxs-lookup"><span data-stu-id="05515-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="05515-119">Seção **Propriedades de gradiente**</span><span class="sxs-lookup"><span data-stu-id="05515-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="05515-120">Seção **Propriedades de bisel**</span><span class="sxs-lookup"><span data-stu-id="05515-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="05515-121">Seção de **Propriedades de efeito adicionais**</span><span class="sxs-lookup"><span data-stu-id="05515-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="05515-122">Seção de **Paradas de gradiente de linha**</span><span class="sxs-lookup"><span data-stu-id="05515-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="05515-123">Seção de **Paradas de gradiente de preenchimento**</span><span class="sxs-lookup"><span data-stu-id="05515-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="05515-124">Para fazer referência à célula **ReplaceLockFormat** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="05515-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05515-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="05515-125">Cell name:</span></span>  <br/> | <span data-ttu-id="05515-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="05515-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="05515-127">Para obter uma referência à célula **ReplaceLockFormat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="05515-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05515-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="05515-128">Section index:</span></span>  <br/> |<span data-ttu-id="05515-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05515-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="05515-130">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="05515-130">Row index:</span></span>  <br/> |<span data-ttu-id="05515-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="05515-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="05515-132">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="05515-132">Cell index:</span></span>  <br/> |<span data-ttu-id="05515-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="05515-133">**visReplaceLockFormat**</span></span> <br/> |
   

