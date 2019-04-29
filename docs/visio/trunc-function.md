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
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426496"
---
# <a name="trunc-function"></a><span data-ttu-id="38e4b-103">Função TRUNC</span><span class="sxs-lookup"><span data-stu-id="38e4b-103">TRUNC Function</span></span>

<span data-ttu-id="38e4b-104">Retorna um número truncado para o número especificado de dígitos.</span><span class="sxs-lookup"><span data-stu-id="38e4b-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="38e4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38e4b-105">Syntax</span></span>

<span data-ttu-id="38e4b-106">TRUNCAr (\* \* *número* \* \*, \* \* *dígitos* \* \*)</span><span class="sxs-lookup"><span data-stu-id="38e4b-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="38e4b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38e4b-107">Parameters</span></span>

|<span data-ttu-id="38e4b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="38e4b-108">**Name**</span></span>|<span data-ttu-id="38e4b-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="38e4b-109">**Required/Optional**</span></span>|<span data-ttu-id="38e4b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="38e4b-110">**Data Type**</span></span>|<span data-ttu-id="38e4b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38e4b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="38e4b-112">_number_</span><span class="sxs-lookup"><span data-stu-id="38e4b-112">_number_</span></span> <br/> |<span data-ttu-id="38e4b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38e4b-113">Required</span></span>  <br/> |<span data-ttu-id="38e4b-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="38e4b-114">**Numeric**</span></span> <br/> |<span data-ttu-id="38e4b-115">O número a ser truncado.</span><span class="sxs-lookup"><span data-stu-id="38e4b-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="38e4b-116">_dígitos_</span><span class="sxs-lookup"><span data-stu-id="38e4b-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="38e4b-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="38e4b-117">Required</span></span>  <br/> |<span data-ttu-id="38e4b-118">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="38e4b-118">**Numeric**</span></span> <br/> |<span data-ttu-id="38e4b-119">O número de dígitos para o qual truncar o _número_.</span><span class="sxs-lookup"><span data-stu-id="38e4b-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="38e4b-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="38e4b-120">Return value</span></span>

<span data-ttu-id="38e4b-121">Numéricos.</span><span class="sxs-lookup"><span data-stu-id="38e4b-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38e4b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="38e4b-122">Remarks</span></span>

<span data-ttu-id="38e4b-123">Se o número de _dígitos_ for maior que 0, o número será truncado para o _número_ de _dígitos_ à direita do decimal.</span><span class="sxs-lookup"><span data-stu-id="38e4b-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="38e4b-124">Se o número de _dígitos_ for 0, _núm_ será truncado para um inteiro.</span><span class="sxs-lookup"><span data-stu-id="38e4b-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="38e4b-125">Se o número de _dígitos_ for menor que 0, o número será truncado para o _número_ de _dígitos_ à esquerda do decimal.</span><span class="sxs-lookup"><span data-stu-id="38e4b-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="38e4b-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38e4b-126">Example 1</span></span>

<span data-ttu-id="38e4b-127">TRUNCAR (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="38e4b-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="38e4b-128">Retornará 123,65.</span><span class="sxs-lookup"><span data-stu-id="38e4b-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="38e4b-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="38e4b-129">Example 2</span></span>

<span data-ttu-id="38e4b-130">TRUNCAR (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="38e4b-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="38e4b-131">Retornará 123.</span><span class="sxs-lookup"><span data-stu-id="38e4b-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="38e4b-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="38e4b-132">Example 3</span></span>

<span data-ttu-id="38e4b-133">TRUNCAR (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="38e4b-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="38e4b-134">Retornará 120.</span><span class="sxs-lookup"><span data-stu-id="38e4b-134">Returns 120.</span></span>
  

