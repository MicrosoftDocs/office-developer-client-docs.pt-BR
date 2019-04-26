---
title: Função DAYOFYEAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Retorna um inteiro, de 1 a 366, que representa o dia sequencial do ano em data e hora ou expressão. A função DAYOFYEAR usa o calendário Gregoriano.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360288"
---
# <a name="dayofyear-function"></a><span data-ttu-id="9862f-104">Função DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9862f-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="9862f-105">Retorna um inteiro, de 1 a 366, que representa o dia sequencial do ano em   _ data e hora_ ou  _expressão_.</span><span class="sxs-lookup"><span data-stu-id="9862f-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="9862f-106">A função DAYOFYEAR usa o calendário Gregoriano.</span><span class="sxs-lookup"><span data-stu-id="9862f-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9862f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9862f-107">Syntax</span></span>

<span data-ttu-id="9862f-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expressão* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="9862f-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9862f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9862f-109">Parameters</span></span>

|<span data-ttu-id="9862f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9862f-110">**Name**</span></span>|<span data-ttu-id="9862f-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="9862f-111">**Required/Optional**</span></span>|<span data-ttu-id="9862f-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9862f-112">**Data Type**</span></span>|<span data-ttu-id="9862f-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9862f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9862f-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="9862f-114">_DateTime_</span></span> <br/> |<span data-ttu-id="9862f-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9862f-115">Required</span></span>  <br/> |<span data-ttu-id="9862f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="9862f-116">**String**</span></span> <br/> |<span data-ttu-id="9862f-117">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="9862f-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="9862f-118">_expressão_</span><span class="sxs-lookup"><span data-stu-id="9862f-118">_expression_</span></span> <br/> |<span data-ttu-id="9862f-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9862f-119">Required</span></span>  <br/> |<span data-ttu-id="9862f-120">**String**</span><span class="sxs-lookup"><span data-stu-id="9862f-120">**String**</span></span> <br/> |<span data-ttu-id="9862f-121">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="9862f-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="9862f-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="9862f-122">_lcid_</span></span> <br/> |<span data-ttu-id="9862f-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="9862f-123">Optional</span></span>  <br/> |<span data-ttu-id="9862f-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="9862f-124">**Number**</span></span> <br/> |<span data-ttu-id="9862f-p103">Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="9862f-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9862f-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9862f-127">Return value</span></span>

<span data-ttu-id="9862f-128">Inteiro</span><span class="sxs-lookup"><span data-stu-id="9862f-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9862f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="9862f-129">Remarks</span></span>

<span data-ttu-id="9862f-130">Qualquer componente de tempo em _datetime_ ou _expression_ é descartado.</span><span class="sxs-lookup"><span data-stu-id="9862f-130">Any time component in _datetime_ or _expression_ is discarded.</span></span> 
  
<span data-ttu-id="9862f-131">O resultado corresponde de 1 de janeiro a 31 de dezembro.</span><span class="sxs-lookup"><span data-stu-id="9862f-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="9862f-132">Não é feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="9862f-132">No rounding is done.</span></span> <span data-ttu-id="9862f-133">Se _datetime_ estiver ausente ou não puder ser interpretado como uma data ou hora válida, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9862f-133">If _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="9862f-134">A função DAYOFYEAR também aceita um único valor numérico para  _expressão_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="9862f-134">The DAYOFYEAR function also accepts a single number value for _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9862f-135">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9862f-135">Example 1</span></span>

<span data-ttu-id="9862f-136">DAYOFYEAR("30 de maio de 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="9862f-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="9862f-137">Retorna 150.</span><span class="sxs-lookup"><span data-stu-id="9862f-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9862f-138">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9862f-138">Example 2</span></span>

<span data-ttu-id="9862f-139">DAYOFYEAR(DATEVALUE("30 de maio de 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="9862f-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="9862f-140">Retornará 157.</span><span class="sxs-lookup"><span data-stu-id="9862f-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9862f-141">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9862f-141">Example 3</span></span>

<span data-ttu-id="9862f-142">DAYOFYEAR (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="9862f-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="9862f-143">Retornará 150.</span><span class="sxs-lookup"><span data-stu-id="9862f-143">Returns 150.</span></span>
  

