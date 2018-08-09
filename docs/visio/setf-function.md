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
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772865"
---
# <a name="setf-function"></a><span data-ttu-id="20dda-103">Função SETF</span><span class="sxs-lookup"><span data-stu-id="20dda-103">SETF Function</span></span>

<span data-ttu-id="20dda-104">Define a fórmula de uma célula.</span><span class="sxs-lookup"><span data-stu-id="20dda-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="20dda-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20dda-105">Syntax</span></span>

<span data-ttu-id="20dda-106">SETF (GETREF (* * *célula* * *), * * *fórmula* * *)</span><span class="sxs-lookup"><span data-stu-id="20dda-106">SETF( GETREF(** *cell* ** ), ** *formula* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20dda-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20dda-107">Parameters</span></span>

|<span data-ttu-id="20dda-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="20dda-108">**Name**</span></span>|<span data-ttu-id="20dda-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="20dda-109">**Required/Optional**</span></span>|<span data-ttu-id="20dda-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="20dda-110">**Data Type**</span></span>|<span data-ttu-id="20dda-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20dda-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20dda-112">_célula_</span><span class="sxs-lookup"><span data-stu-id="20dda-112">_cell_</span></span> <br/> |<span data-ttu-id="20dda-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="20dda-113">Required</span></span>  <br/> |<span data-ttu-id="20dda-114">**String**</span><span class="sxs-lookup"><span data-stu-id="20dda-114">**String**</span></span> <br/> |<span data-ttu-id="20dda-115">A célula cuja fórmula deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="20dda-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="20dda-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="20dda-116">_formula_</span></span> <br/> |<span data-ttu-id="20dda-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="20dda-117">Required</span></span>  <br/> |<span data-ttu-id="20dda-118">**String**</span><span class="sxs-lookup"><span data-stu-id="20dda-118">**String**</span></span> <br/> |<span data-ttu-id="20dda-119">A fórmula a ser usada.</span><span class="sxs-lookup"><span data-stu-id="20dda-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20dda-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="20dda-120">Remarks</span></span>

<span data-ttu-id="20dda-121">Quando avaliada, o resultado da expressão na _fórmula_ torna-se a nova fórmula na _célula_.</span><span class="sxs-lookup"><span data-stu-id="20dda-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="20dda-122">Se a _fórmula_ está entre aspas, a expressão entre aspas foi escrita para a _célula_.</span><span class="sxs-lookup"><span data-stu-id="20dda-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="20dda-123">Para definir a _célula_ como uma cadeia de caracteres, coloque a _fórmula_ em três conjuntos de aspas.</span><span class="sxs-lookup"><span data-stu-id="20dda-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="20dda-p102">A célula de destino deve ser especificada usando-se uma referência GETREF() ou uma cadeia de caracteres para evitar a circularidade. É preferível usar GETREF, porque o Microsoft Visio pode ajustar as referências quando a forma é movida para um documento diferente.</span><span class="sxs-lookup"><span data-stu-id="20dda-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="20dda-126">Se a _célula_ não for especificado, usando GETREF ou como uma cadeia de caracteres, a função retornará um erro e fórmula da célula não é alterada.</span><span class="sxs-lookup"><span data-stu-id="20dda-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="20dda-127">Se a _fórmula_ contém um erro de sintaxe, a função retornará um erro e a fórmula na _célula_ não será alterada.</span><span class="sxs-lookup"><span data-stu-id="20dda-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="20dda-128">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20dda-128">Example 1</span></span>

<span data-ttu-id="20dda-129">SETF (GETREF(Scratch.A1), 1,5 pol \* 6 + 1 pé)</span><span class="sxs-lookup"><span data-stu-id="20dda-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="20dda-130">Define a fórmula de Scratch.A1 para 21 polegadas.</span><span class="sxs-lookup"><span data-stu-id="20dda-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="20dda-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="20dda-131">Example 2</span></span>

<span data-ttu-id="20dda-132">SETF (GETREF(Scratch.A1), "1,5 pol \* 6 + 1 pé")</span><span class="sxs-lookup"><span data-stu-id="20dda-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="20dda-133">Define a fórmula do zero.</span><span class="sxs-lookup"><span data-stu-id="20dda-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="20dda-134">A1 à expressão 1,5 na\*6 + 1 pé.</span><span class="sxs-lookup"><span data-stu-id="20dda-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="20dda-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="20dda-135">Example 3</span></span>

<span data-ttu-id="20dda-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="20dda-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="20dda-137">Define a fórmula de Scratch.A1 para a sequência de caracteres "Say ""ahh""" que avalia para Say "ahh".</span><span class="sxs-lookup"><span data-stu-id="20dda-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

