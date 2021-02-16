---
title: Função DAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Retorna um número inteiro, de 1 a 31, representando o dia em datetime ou expression. A função DAY usa o calendário gregoriano.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360289"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="a8596-104">Função DAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a8596-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a8596-105">Retorna um número inteiro, de 1 a 31, representando o dia em _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="a8596-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="a8596-106">A função DAY usa o calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="a8596-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a8596-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8596-107">Syntax</span></span>

<span data-ttu-id="a8596-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="a8596-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a8596-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8596-109">Parameters</span></span>

|<span data-ttu-id="a8596-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a8596-110">**Name**</span></span>|<span data-ttu-id="a8596-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a8596-111">**Required/Optional**</span></span>|<span data-ttu-id="a8596-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a8596-112">**Data Type**</span></span>|<span data-ttu-id="a8596-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a8596-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a8596-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="a8596-114">_datetime_</span></span> <br/> |<span data-ttu-id="a8596-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a8596-115">Required</span></span>  <br/> |<span data-ttu-id="a8596-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a8596-116">**String**</span></span> <br/> |<span data-ttu-id="a8596-117">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="a8596-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a8596-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="a8596-118">_expression_</span></span> <br/> |<span data-ttu-id="a8596-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a8596-119">Required</span></span>  <br/> |<span data-ttu-id="a8596-120">**String**</span><span class="sxs-lookup"><span data-stu-id="a8596-120">**String**</span></span> <br/> |<span data-ttu-id="a8596-121">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="a8596-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a8596-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a8596-122">_lcid_</span></span> <br/> |<span data-ttu-id="a8596-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="a8596-123">Optional</span></span>  <br/> |<span data-ttu-id="a8596-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="a8596-124">**Number**</span></span> <br/> |<span data-ttu-id="a8596-p103">Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="a8596-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a8596-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a8596-127">Return value</span></span>

<span data-ttu-id="a8596-128">Inteiro</span><span class="sxs-lookup"><span data-stu-id="a8596-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8596-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8596-129">Remarks</span></span>

<span data-ttu-id="a8596-130">Qualquer componente de tempo em _datetime_ ou _expression_ é descartado.</span><span class="sxs-lookup"><span data-stu-id="a8596-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a8596-131">Não são feitos arredondamentos.</span><span class="sxs-lookup"><span data-stu-id="a8596-131">No rounding is done.</span></span> <span data-ttu-id="a8596-132">Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a8596-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="a8596-133">A função DAY também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="a8596-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a8596-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8596-134">Example 1</span></span>

<span data-ttu-id="a8596-135">DAY("30 de maio de 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="a8596-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="a8596-136">Retornará 30.</span><span class="sxs-lookup"><span data-stu-id="a8596-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a8596-137">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a8596-137">Example 2</span></span>

<span data-ttu-id="a8596-138">DAY(DATEVALUE("30 de maio de 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="a8596-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="a8596-139">Retornará 6.</span><span class="sxs-lookup"><span data-stu-id="a8596-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a8596-140">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a8596-140">Example 3</span></span>

<span data-ttu-id="a8596-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="a8596-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="a8596-142">Retornará 30.</span><span class="sxs-lookup"><span data-stu-id="a8596-142">Returns 30.</span></span>
  

