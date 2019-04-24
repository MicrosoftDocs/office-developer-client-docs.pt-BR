---
title: Função CY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Retorna um valor de moeda.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344986"
---
# <a name="cy-function"></a><span data-ttu-id="059e5-103">Função CY</span><span class="sxs-lookup"><span data-stu-id="059e5-103">CY Function</span></span>

<span data-ttu-id="059e5-104">Retorna um valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="059e5-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="059e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="059e5-105">Syntax</span></span>

<span data-ttu-id="059e5-106">CY (\* \* *valor* \* \*, \* \* *cyID* \* \*)</span><span class="sxs-lookup"><span data-stu-id="059e5-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="059e5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="059e5-107">Parameters</span></span>

|<span data-ttu-id="059e5-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="059e5-108">**Name**</span></span>|<span data-ttu-id="059e5-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="059e5-109">**Required/Optional**</span></span>|<span data-ttu-id="059e5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="059e5-110">**Data Type**</span></span>|<span data-ttu-id="059e5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="059e5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="059e5-112">_value_</span><span class="sxs-lookup"><span data-stu-id="059e5-112">_value_</span></span> <br/> |<span data-ttu-id="059e5-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="059e5-113">Optional</span></span>  <br/> |<span data-ttu-id="059e5-114">**Número ou Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="059e5-114">**Number or String**</span></span> <br/> |<span data-ttu-id="059e5-115">Um número ou uma cadeia de caracteres que inclui formatação específica da moeda.</span><span class="sxs-lookup"><span data-stu-id="059e5-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="059e5-116">Se não for especificado, o valor de moeda é formatado de acordo com o estilo de moeda nas configurações de idioma e região do sistema.</span><span class="sxs-lookup"><span data-stu-id="059e5-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="059e5-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="059e5-117">_cyID_</span></span> <br/> |<span data-ttu-id="059e5-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="059e5-118">Optional</span></span>  <br/> |<span data-ttu-id="059e5-119">**Número**</span><span class="sxs-lookup"><span data-stu-id="059e5-119">**Number**</span></span> <br/> |<span data-ttu-id="059e5-120">Uma ID de moeda numérica ou uma cadeia de caracteres entre aspas de três caracteres para a abreviação ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="059e5-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="059e5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="059e5-121">Remarks</span></span>

<span data-ttu-id="059e5-122">Para especificar uma moeda diferente, você deve incluir um _cyID_válido.</span><span class="sxs-lookup"><span data-stu-id="059e5-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="059e5-123">Para obter uma lista, consulte [Sobre constantes de moeda](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="059e5-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="059e5-124">Se o _valor_ for incompatível com o tipo de moeda designada ou se um argumento inválido, como "não um número", for especificado, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="059e5-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="059e5-125">será retornado.</span><span class="sxs-lookup"><span data-stu-id="059e5-125">error is returned.</span></span> <span data-ttu-id="059e5-126">Se o _valor_ for maior que 922337203685477,5807 ou menor que-922337203685477,5808, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="059e5-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="059e5-127">será retornado.</span><span class="sxs-lookup"><span data-stu-id="059e5-127">error is returned.</span></span> 
  
<span data-ttu-id="059e5-128">Para maior precisão com valores de moeda muito grandes que incluem frações de uma unidade, como 3.600.000.000.000, use argumentos de cadeia de caracteres para _Value_.</span><span class="sxs-lookup"><span data-stu-id="059e5-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="059e5-129">A especificação de um _cyID_ inválido retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="059e5-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="059e5-130">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="059e5-130">Example 1</span></span>

<span data-ttu-id="059e5-131">No caso das configurações de Região e Idioma do usuário, especifique dólares dos Estados Unidos:</span><span class="sxs-lookup"><span data-stu-id="059e5-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="059e5-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="059e5-132">CY(999998.993)</span></span>
  
<span data-ttu-id="059e5-133">Retornará $999.998,99</span><span class="sxs-lookup"><span data-stu-id="059e5-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="059e5-134">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="059e5-134">Example 2</span></span>

<span data-ttu-id="059e5-135">CY(12345678,.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="059e5-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="059e5-136">Retornará $12.345.678,99</span><span class="sxs-lookup"><span data-stu-id="059e5-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="059e5-137">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="059e5-137">Example 3</span></span>

<span data-ttu-id="059e5-138">CY(12345678,993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="059e5-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="059e5-139">Retornará 12.345.678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="059e5-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="059e5-140">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="059e5-140">Example 4</span></span>

<span data-ttu-id="059e5-141">CY(12345678,7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="059e5-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="059e5-142">Retornará 12.345.678,78</span><span class="sxs-lookup"><span data-stu-id="059e5-142">Returns 12,345,678.78</span></span>
  

