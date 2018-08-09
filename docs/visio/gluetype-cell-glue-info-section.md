---
title: Célula GlueType (Seção Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Determina se uma forma 1D utilizará a cola estática (ponto a ponto) ou dinâmica (forma a forma) ao ser colada em outra forma.
ms.openlocfilehash: 162827521cda6fe4a37d17a8f7d36d7a36718519
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771973"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="30237-103">Célula GlueType (Seção Glue Info)</span><span class="sxs-lookup"><span data-stu-id="30237-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="30237-104">Determina se uma forma 1D utilizará a cola estática (ponto a ponto) ou dinâmica (forma a forma) ao ser colada em outra forma.</span><span class="sxs-lookup"><span data-stu-id="30237-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="30237-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="30237-105">**Value**</span></span>|<span data-ttu-id="30237-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30237-106">**Description**</span></span>|<span data-ttu-id="30237-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="30237-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="30237-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="30237-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="30237-p101">Padrão. Permitir cola dinâmica somente para o conector dinâmico; caso contrário, utilizar cola estática.</span><span class="sxs-lookup"><span data-stu-id="30237-p101">Default. Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="30237-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="30237-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="30237-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="30237-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="30237-113">Permitir cola dinâmica.</span><span class="sxs-lookup"><span data-stu-id="30237-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="30237-114">Obsoleta no Visio 2002</span><span class="sxs-lookup"><span data-stu-id="30237-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="30237-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="30237-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="30237-116">Permitir cola dinâmica.</span><span class="sxs-lookup"><span data-stu-id="30237-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="30237-117">**visGlueTypeWalking**</span><span class="sxs-lookup"><span data-stu-id="30237-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="30237-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="30237-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="30237-119">Não permitir cola dinâmica.</span><span class="sxs-lookup"><span data-stu-id="30237-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="30237-120">**visGlueTypeNoWalking**</span><span class="sxs-lookup"><span data-stu-id="30237-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="30237-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="30237-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="30237-122">Não permitir que esta forma 2D seja conectada com cola dinâmica.</span><span class="sxs-lookup"><span data-stu-id="30237-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="30237-123">**visGlueTypeNoWalkingTo**</span><span class="sxs-lookup"><span data-stu-id="30237-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30237-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="30237-124">Remarks</span></span>

<span data-ttu-id="30237-125">Se esta célula contiver valores de 1, 2 ou 3, a cola dinâmica será estabelecida quando um destes procedimentos ocorrer:</span><span class="sxs-lookup"><span data-stu-id="30237-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="30237-126">As formas estão coladas dinamicamente na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="30237-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="30237-127">As formas estão coladas nas células PinX ou PinY de outra forma a partir de um programa.</span><span class="sxs-lookup"><span data-stu-id="30237-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="30237-128">Se as formas estiverem coladas em células de forma diferentes de PinX ou PinY a partir de um programa, a cola estática será utilizada.</span><span class="sxs-lookup"><span data-stu-id="30237-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="30237-p102">A alteração desse valor de permitir para não permitir a cola dinâmica não corta ou altera a cola dinâmica existente. Os programas podem estabelecer a cola dinâmica mesmo se ela estiver desabilitada na célula GlueType.</span><span class="sxs-lookup"><span data-stu-id="30237-p102">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue. Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="30237-131">Para fazer referência à célula GlueType pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="30237-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30237-132">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="30237-132">Cell name:</span></span>  <br/> | <span data-ttu-id="30237-133">GlueType</span><span class="sxs-lookup"><span data-stu-id="30237-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="30237-134">Para fazer referência à célula GlueType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="30237-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30237-135">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="30237-135">Section index:</span></span>  <br/> |<span data-ttu-id="30237-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30237-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30237-137">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="30237-137">Row index:</span></span>  <br/> |<span data-ttu-id="30237-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="30237-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="30237-139">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="30237-139">Cell index:</span></span>  <br/> |<span data-ttu-id="30237-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="30237-140">**visGlueType**</span></span> <br/> |
   
