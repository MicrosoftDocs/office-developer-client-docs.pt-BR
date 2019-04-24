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
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315572"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="47283-103">Função ROUND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="47283-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="47283-104">Arredonda um número para a precisão representada pelo número de *dígitos* .</span><span class="sxs-lookup"><span data-stu-id="47283-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="47283-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47283-105">Syntax</span></span>

<span data-ttu-id="47283-106">ARREd (\* \* Number \* \*, \* \* *número* de *dígitos* \* \*)</span><span class="sxs-lookup"><span data-stu-id="47283-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="47283-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47283-107">Parameters</span></span>

|<span data-ttu-id="47283-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="47283-108">**Name**</span></span>|<span data-ttu-id="47283-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="47283-109">**Required/Optional**</span></span>|<span data-ttu-id="47283-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="47283-110">**Data Type**</span></span>|<span data-ttu-id="47283-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47283-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="47283-112">_number_</span><span class="sxs-lookup"><span data-stu-id="47283-112">_number_</span></span> <br/> |<span data-ttu-id="47283-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="47283-113">Required</span></span>  <br/> |<span data-ttu-id="47283-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="47283-114">**Number**</span></span> <br/> |<span data-ttu-id="47283-115">O número a ser arredondado.</span><span class="sxs-lookup"><span data-stu-id="47283-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="47283-116">_dígitos_</span><span class="sxs-lookup"><span data-stu-id="47283-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="47283-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="47283-117">Required</span></span>  <br/> |<span data-ttu-id="47283-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="47283-118">**Number**</span></span> <br/> |<span data-ttu-id="47283-119">O número de casas decimais de precisão.</span><span class="sxs-lookup"><span data-stu-id="47283-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47283-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="47283-120">Remarks</span></span>

<span data-ttu-id="47283-121">Se o número de _dígitos_ for maior que 0, núm será arredondado para o _número_ de _dígitos_ à direita do decimal.</span><span class="sxs-lookup"><span data-stu-id="47283-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="47283-122">Se o número de _dígitos_ for 0, _núm_ será arredondado para um inteiro.</span><span class="sxs-lookup"><span data-stu-id="47283-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="47283-123">Se o número de _dígitos_ for menor que 0, núm será arredondado para o _número_ de _dígitos_ à esquerda do decimal.</span><span class="sxs-lookup"><span data-stu-id="47283-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="47283-124">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47283-124">Example 1</span></span>

<span data-ttu-id="47283-125">ARRED (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="47283-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="47283-126">Retornará 123,65.</span><span class="sxs-lookup"><span data-stu-id="47283-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="47283-127">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47283-127">Example 2</span></span>

<span data-ttu-id="47283-128">ARRED (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="47283-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="47283-129">Retornará 124.</span><span class="sxs-lookup"><span data-stu-id="47283-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="47283-130">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="47283-130">Example 3</span></span>

<span data-ttu-id="47283-131">ARRED (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="47283-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="47283-132">Retornará 120.</span><span class="sxs-lookup"><span data-stu-id="47283-132">Returns 120.</span></span>
  

