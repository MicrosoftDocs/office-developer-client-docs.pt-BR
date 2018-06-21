---
title: Função ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arredonda um número para a precisão representada pelo número de dígitos.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19772752"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="106c3-103">Função ROUND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="106c3-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="106c3-104">Arredonda um número para a precisão representada pelo *número de dígitos* .</span><span class="sxs-lookup"><span data-stu-id="106c3-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="106c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="106c3-105">Syntax</span></span>

<span data-ttu-id="106c3-106">Arredondar (* * *número* * *, * * *número de dígitos* * *)</span><span class="sxs-lookup"><span data-stu-id="106c3-106">ROUND(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="106c3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="106c3-107">Parameters</span></span>

|<span data-ttu-id="106c3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="106c3-108">**Name**</span></span>|<span data-ttu-id="106c3-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="106c3-109">**Required/Optional**</span></span>|<span data-ttu-id="106c3-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="106c3-110">**Data Type**</span></span>|<span data-ttu-id="106c3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="106c3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="106c3-112">_number_</span><span class="sxs-lookup"><span data-stu-id="106c3-112">_number_</span></span> <br/> |<span data-ttu-id="106c3-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="106c3-113">Required</span></span>  <br/> |<span data-ttu-id="106c3-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="106c3-114">**Number**</span></span> <br/> |<span data-ttu-id="106c3-115">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="106c3-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="106c3-116">_número de dígitos_</span><span class="sxs-lookup"><span data-stu-id="106c3-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="106c3-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="106c3-117">Required</span></span>  <br/> |<span data-ttu-id="106c3-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="106c3-118">**Number**</span></span> <br/> |<span data-ttu-id="106c3-119">O número de casas decimais de precisão.</span><span class="sxs-lookup"><span data-stu-id="106c3-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="106c3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="106c3-120">Remarks</span></span>

<span data-ttu-id="106c3-121">Se o _número de dígitos_ for maior do que 0, o _número_ será arredondado pelo _número de dígitos_ à direita da vírgula decimal.</span><span class="sxs-lookup"><span data-stu-id="106c3-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="106c3-122">Se o _número de dígitos_ for 0, o _número_ será arredondado para um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="106c3-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="106c3-123">Se o _número de dígitos_ for menor que 0, o _número_ será arredondado pelo _número de dígitos_ à esquerda da vírgula decimal.</span><span class="sxs-lookup"><span data-stu-id="106c3-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="106c3-124">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="106c3-124">Example 1</span></span>

<span data-ttu-id="106c3-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="106c3-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="106c3-126">Retornará 123,65.</span><span class="sxs-lookup"><span data-stu-id="106c3-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="106c3-127">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="106c3-127">Example 2</span></span>

<span data-ttu-id="106c3-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="106c3-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="106c3-129">Retornará 124.</span><span class="sxs-lookup"><span data-stu-id="106c3-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="106c3-130">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="106c3-130">Example 3</span></span>

<span data-ttu-id="106c3-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="106c3-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="106c3-132">Retornará 120.</span><span class="sxs-lookup"><span data-stu-id="106c3-132">Returns 120.</span></span>
  

