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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433553"
---
# <a name="cy-function"></a><span data-ttu-id="af260-103">Função CY</span><span class="sxs-lookup"><span data-stu-id="af260-103">CY Function</span></span>

<span data-ttu-id="af260-104">Retorna um valor de moeda.</span><span class="sxs-lookup"><span data-stu-id="af260-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="af260-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af260-105">Syntax</span></span>

<span data-ttu-id="af260-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span><span class="sxs-lookup"><span data-stu-id="af260-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="af260-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af260-107">Parameters</span></span>

|<span data-ttu-id="af260-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="af260-108">**Name**</span></span>|<span data-ttu-id="af260-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="af260-109">**Required/Optional**</span></span>|<span data-ttu-id="af260-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="af260-110">**Data Type**</span></span>|<span data-ttu-id="af260-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="af260-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="af260-112">_value_</span><span class="sxs-lookup"><span data-stu-id="af260-112">_value_</span></span> <br/> |<span data-ttu-id="af260-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="af260-113">Optional</span></span>  <br/> |<span data-ttu-id="af260-114">**Número ou Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="af260-114">**Number or String**</span></span> <br/> |<span data-ttu-id="af260-115">Um número ou uma cadeia de caracteres que inclui formatação específica de moeda.</span><span class="sxs-lookup"><span data-stu-id="af260-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="af260-116">Se não for especificado, o valor de moeda será formatado de acordo com o estilo de moeda nas configurações de Região e Idioma do sistema.</span><span class="sxs-lookup"><span data-stu-id="af260-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="af260-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="af260-117">_cyID_</span></span> <br/> |<span data-ttu-id="af260-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="af260-118">Optional</span></span>  <br/> |<span data-ttu-id="af260-119">**Número**</span><span class="sxs-lookup"><span data-stu-id="af260-119">**Number**</span></span> <br/> |<span data-ttu-id="af260-120">Uma ID de moeda numérica ou uma cadeia de caracteres entre aspas de três caracteres para a abreviação ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="af260-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af260-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="af260-121">Remarks</span></span>

<span data-ttu-id="af260-122">Para especificar uma moeda diferente, você deve incluir uma _cyID válida._</span><span class="sxs-lookup"><span data-stu-id="af260-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="af260-123">Para obter uma lista, consulte [Sobre constantes de moeda](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="af260-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="af260-124">Se  _o_ valor for incompatível com o tipo de moeda designado ou se um argumento inválido como "não for um número" for especificado, uma #VALUE!</span><span class="sxs-lookup"><span data-stu-id="af260-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="af260-125">será retornado.</span><span class="sxs-lookup"><span data-stu-id="af260-125">error is returned.</span></span> <span data-ttu-id="af260-126">Se  o valor for maior que 922.337.203.685.477.5807 ou menor que -922.337.203.685.477.5808, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="af260-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="af260-127">será retornado.</span><span class="sxs-lookup"><span data-stu-id="af260-127">error is returned.</span></span> 
  
<span data-ttu-id="af260-128">Para melhor precisão com valores monetários muito grandes que incluem frações de uma unidade, como 3,6 trilhões, use argumentos de cadeia de caracteres como _valor._</span><span class="sxs-lookup"><span data-stu-id="af260-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="af260-129">Especificar uma  _cyID inválida_ retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="af260-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="af260-130">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af260-130">Example 1</span></span>

<span data-ttu-id="af260-131">No caso das configurações de Região e Idioma do usuário, especifique dólares dos Estados Unidos:</span><span class="sxs-lookup"><span data-stu-id="af260-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="af260-132">CY(999998,993)</span><span class="sxs-lookup"><span data-stu-id="af260-132">CY(999998.993)</span></span>
  
<span data-ttu-id="af260-133">Retornará $999.998,99</span><span class="sxs-lookup"><span data-stu-id="af260-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="af260-134">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af260-134">Example 2</span></span>

<span data-ttu-id="af260-135">CY(12345678,.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="af260-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="af260-136">Retornará $12.345.678,99</span><span class="sxs-lookup"><span data-stu-id="af260-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="af260-137">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="af260-137">Example 3</span></span>

<span data-ttu-id="af260-138">CY(12345678,993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="af260-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="af260-139">Retornará 12.345.678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="af260-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="af260-140">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="af260-140">Example 4</span></span>

<span data-ttu-id="af260-141">CY(12345678,7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="af260-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="af260-142">Retornará 12.345.678,78</span><span class="sxs-lookup"><span data-stu-id="af260-142">Returns 12,345,678.78</span></span>
  

