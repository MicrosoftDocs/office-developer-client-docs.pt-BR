---
title: Função SECOND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Retorna um inteiro, 0 a 59, que representa o componente de segundos de DateTime ou expressão.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404873"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="18155-103">Função SECOND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="18155-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="18155-104">Retorna um inteiro, 0 a 59, que representa o componente de segundos de _DateTime_ ou _expressão_.</span><span class="sxs-lookup"><span data-stu-id="18155-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="18155-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18155-105">Syntax</span></span>

<span data-ttu-id="18155-106">SEGUNDO ("\* \* *DateTime* \* \*" | \* \* *expressão* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="18155-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="18155-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18155-107">Parameters</span></span>

|<span data-ttu-id="18155-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="18155-108">**Name**</span></span>|<span data-ttu-id="18155-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="18155-109">**Required/Optional**</span></span>|<span data-ttu-id="18155-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="18155-110">**Data Type**</span></span>|<span data-ttu-id="18155-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18155-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="18155-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="18155-112">_datetime_</span></span> <br/> |<span data-ttu-id="18155-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="18155-113">Required</span></span>  <br/> |<span data-ttu-id="18155-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18155-114">**String**</span></span> <br/> |<span data-ttu-id="18155-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="18155-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="18155-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="18155-116">_expression_</span></span> <br/> |<span data-ttu-id="18155-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="18155-117">Required</span></span>  <br/> |<span data-ttu-id="18155-118">**String**</span><span class="sxs-lookup"><span data-stu-id="18155-118">**String**</span></span> <br/> | <span data-ttu-id="18155-119">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="18155-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="18155-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="18155-120">_lcid_</span></span> <br/> |<span data-ttu-id="18155-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="18155-121">Optional</span></span>  <br/> |<span data-ttu-id="18155-122">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="18155-122">**Numeric**</span></span> <br/> |<span data-ttu-id="18155-123">O identificador de localidade a ser usado na avaliação de um _DateTime_não local.</span><span class="sxs-lookup"><span data-stu-id="18155-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="18155-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="18155-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="18155-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18155-125">Return value</span></span>

<span data-ttu-id="18155-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="18155-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18155-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="18155-127">Remarks</span></span>

<span data-ttu-id="18155-128">O componente de data em _DateTime_ ou _expression_ é Descartado.</span><span class="sxs-lookup"><span data-stu-id="18155-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="18155-129">Não é feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="18155-129">No rounding is done.</span></span> <span data-ttu-id="18155-130">Se a _data/hora_ estiver ausente ou não puder ser convertida em um resultado válido, essa função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="18155-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="18155-131">A segunda função também aceita um valor de número único para _expressão_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="18155-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="18155-132">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18155-132">Example 1</span></span>

<span data-ttu-id="18155-133">SEGUNDO ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="18155-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="18155-134">Retornará 32.</span><span class="sxs-lookup"><span data-stu-id="18155-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="18155-135">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18155-135">Example 2</span></span>

<span data-ttu-id="18155-136">SECOND(TIMEVALUE("30 de maio de 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="18155-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="18155-137">Retornará 52.</span><span class="sxs-lookup"><span data-stu-id="18155-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="18155-138">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="18155-138">Example 3</span></span>

<span data-ttu-id="18155-139">SEGUNDO (0.6337)</span><span class="sxs-lookup"><span data-stu-id="18155-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="18155-140">Retornará 32.</span><span class="sxs-lookup"><span data-stu-id="18155-140">Returns 32.</span></span>
  

