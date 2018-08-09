---
title: Função TRUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Retorna um número truncado para o número especificado de dígitos.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773180"
---
# <a name="trunc-function"></a><span data-ttu-id="e390d-103">Função TRUNC</span><span class="sxs-lookup"><span data-stu-id="e390d-103">TRUNC Function</span></span>

<span data-ttu-id="e390d-104">Retorna um número truncado para o número especificado de dígitos.</span><span class="sxs-lookup"><span data-stu-id="e390d-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e390d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e390d-105">Syntax</span></span>

<span data-ttu-id="e390d-106">TRUNC (* * *número* * *, * * *número de dígitos* * *)</span><span class="sxs-lookup"><span data-stu-id="e390d-106">TRUNC(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e390d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e390d-107">Parameters</span></span>

|<span data-ttu-id="e390d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e390d-108">**Name**</span></span>|<span data-ttu-id="e390d-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e390d-109">**Required/Optional**</span></span>|<span data-ttu-id="e390d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e390d-110">**Data Type**</span></span>|<span data-ttu-id="e390d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e390d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e390d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e390d-112">_number_</span></span> <br/> |<span data-ttu-id="e390d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e390d-113">Required</span></span>  <br/> |<span data-ttu-id="e390d-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="e390d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e390d-115">O número a ser truncado.</span><span class="sxs-lookup"><span data-stu-id="e390d-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="e390d-116">_número de dígitos_</span><span class="sxs-lookup"><span data-stu-id="e390d-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="e390d-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e390d-117">Required</span></span>  <br/> |<span data-ttu-id="e390d-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="e390d-118">**Numeric**</span></span> <br/> |<span data-ttu-id="e390d-119">O número de dígitos para o qual truncar _number_.</span><span class="sxs-lookup"><span data-stu-id="e390d-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e390d-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e390d-120">Return value</span></span>

<span data-ttu-id="e390d-121">Numérico.</span><span class="sxs-lookup"><span data-stu-id="e390d-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e390d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e390d-122">Remarks</span></span>

<span data-ttu-id="e390d-123">Se o _número de dígitos_ for maior do que 0, o _número_ será truncada para o _número de dígitos_ à direita da vírgula decimal.</span><span class="sxs-lookup"><span data-stu-id="e390d-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="e390d-124">Se o _número de dígitos_ for 0, o _número_ será truncada para um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="e390d-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="e390d-125">Se o _número de dígitos_ for menor que 0, o _número_ será truncada para o _número de dígitos_ à esquerda da vírgula decimal.</span><span class="sxs-lookup"><span data-stu-id="e390d-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e390d-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e390d-126">Example 1</span></span>

<span data-ttu-id="e390d-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="e390d-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="e390d-128">Retornará 123,65.</span><span class="sxs-lookup"><span data-stu-id="e390d-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e390d-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e390d-129">Example 2</span></span>

<span data-ttu-id="e390d-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="e390d-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="e390d-131">Retornará 123.</span><span class="sxs-lookup"><span data-stu-id="e390d-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e390d-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e390d-132">Example 3</span></span>

<span data-ttu-id="e390d-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="e390d-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="e390d-134">Retornará 120.</span><span class="sxs-lookup"><span data-stu-id="e390d-134">Returns 120.</span></span>
  

