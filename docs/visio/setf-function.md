---
title: Função SETF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Define a fórmula de uma célula.
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425971"
---
# <a name="setf-function"></a><span data-ttu-id="cd9bc-103">Função SETF</span><span class="sxs-lookup"><span data-stu-id="cd9bc-103">SETF Function</span></span>

<span data-ttu-id="cd9bc-104">Define a fórmula de uma célula.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cd9bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd9bc-105">Syntax</span></span>

<span data-ttu-id="cd9bc-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span><span class="sxs-lookup"><span data-stu-id="cd9bc-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cd9bc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd9bc-107">Parameters</span></span>

|<span data-ttu-id="cd9bc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd9bc-108">**Name**</span></span>|<span data-ttu-id="cd9bc-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="cd9bc-109">**Required/Optional**</span></span>|<span data-ttu-id="cd9bc-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="cd9bc-110">**Data Type**</span></span>|<span data-ttu-id="cd9bc-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cd9bc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cd9bc-112">_cell_</span><span class="sxs-lookup"><span data-stu-id="cd9bc-112">_cell_</span></span> <br/> |<span data-ttu-id="cd9bc-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd9bc-113">Required</span></span>  <br/> |<span data-ttu-id="cd9bc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cd9bc-114">**String**</span></span> <br/> |<span data-ttu-id="cd9bc-115">A célula cuja fórmula definir.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="cd9bc-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="cd9bc-116">_formula_</span></span> <br/> |<span data-ttu-id="cd9bc-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd9bc-117">Required</span></span>  <br/> |<span data-ttu-id="cd9bc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="cd9bc-118">**String**</span></span> <br/> |<span data-ttu-id="cd9bc-119">A fórmula a ser usada.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd9bc-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd9bc-120">Remarks</span></span>

<span data-ttu-id="cd9bc-121">Quando avaliado, o resultado da expressão _na_ fórmula se torna a nova fórmula na _célula._</span><span class="sxs-lookup"><span data-stu-id="cd9bc-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="cd9bc-122">Se _a_ fórmula estiver entre aspas, a expressão entre aspas será escrita na _célula._</span><span class="sxs-lookup"><span data-stu-id="cd9bc-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="cd9bc-123">Para definir  _a célula_ como uma cadeia de caracteres, coloque a  _fórmula_ em três conjuntos de aspas.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="cd9bc-p102">A célula de destino deve ser especificada usando-se uma referência GETREF() ou uma cadeia de caracteres para evitar a circularidade. É preferível usar GETREF, porque o Microsoft Visio pode ajustar as referências quando a forma é movida para um documento diferente.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="cd9bc-126">Se  _a_ célula não for especificada usando GETREF ou como uma cadeia de caracteres, a função retornará um erro e nenhuma fórmula da célula será alterada.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="cd9bc-127">Se  _a_ fórmula contiver um erro de sintaxe, a função retornará um erro e a fórmula na  _célula_ não será alterada.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cd9bc-128">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd9bc-128">Example 1</span></span>

<span data-ttu-id="cd9bc-129">SETF( GETREF(Scratch.A1), 1,5 in \* 6 + 1 pé)</span><span class="sxs-lookup"><span data-stu-id="cd9bc-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="cd9bc-130">Define a fórmula de Scratch.A1 para 21 polegadas.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cd9bc-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd9bc-131">Example 2</span></span>

<span data-ttu-id="cd9bc-132">SETF( GETREF(Scratch.A1), "1,5 in \* 6 + 1 pé")</span><span class="sxs-lookup"><span data-stu-id="cd9bc-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="cd9bc-133">Define a fórmula de Scratch.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="cd9bc-134">A1 para a expressão 1,5 em \* 6+1 pé.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="cd9bc-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cd9bc-135">Example 3</span></span>

<span data-ttu-id="cd9bc-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="cd9bc-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="cd9bc-137">Define a fórmula de Scratch.A1 para a sequência de caracteres "Say ""ahh""" que avalia para Say "ahh".</span><span class="sxs-lookup"><span data-stu-id="cd9bc-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

