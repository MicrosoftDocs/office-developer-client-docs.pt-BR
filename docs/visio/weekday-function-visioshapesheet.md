---
title: Função WEEKDAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Retorna um inteiro, de 1 a 7, representando o dia da semana em data e hora ou expressão.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404803"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="be10f-103">Função WEEKDAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="be10f-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="be10f-104">Retorna um inteiro, de 1 a 7, representando o dia da semana em _data e hora_ ou _expressão._</span><span class="sxs-lookup"><span data-stu-id="be10f-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="be10f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be10f-105">Syntax</span></span>

<span data-ttu-id="be10f-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expressão* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="be10f-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="be10f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be10f-107">Parameters</span></span>

|<span data-ttu-id="be10f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="be10f-108">**Name**</span></span>|<span data-ttu-id="be10f-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="be10f-109">**Required/Optional**</span></span>|<span data-ttu-id="be10f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="be10f-110">**Data Type**</span></span>|<span data-ttu-id="be10f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be10f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="be10f-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="be10f-112">_datetime_</span></span> <br/> |<span data-ttu-id="be10f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="be10f-113">Required</span></span>  <br/> |<span data-ttu-id="be10f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="be10f-114">**String**</span></span> <br/> | <span data-ttu-id="be10f-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="be10f-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="be10f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="be10f-116">_expression_</span></span> <br/> |<span data-ttu-id="be10f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="be10f-117">Required</span></span>  <br/> |<span data-ttu-id="be10f-118">**Varia**</span><span class="sxs-lookup"><span data-stu-id="be10f-118">**Varies**</span></span> <br/> |<span data-ttu-id="be10f-119">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="be10f-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="be10f-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="be10f-120">_lcid_</span></span> <br/> |<span data-ttu-id="be10f-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="be10f-121">Optional</span></span>  <br/> |<span data-ttu-id="be10f-122">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="be10f-122">**Numeric**</span></span> <br/> |<span data-ttu-id="be10f-123">O identificador de local a ser utilizado na avaliação de uma data e hora não locais.</span><span class="sxs-lookup"><span data-stu-id="be10f-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="be10f-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="be10f-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="be10f-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="be10f-125">Return value</span></span>

<span data-ttu-id="be10f-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="be10f-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be10f-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="be10f-127">Remarks</span></span>

<span data-ttu-id="be10f-128">O componente de hora na  _data e_ na  _expressão_ é descartado.</span><span class="sxs-lookup"><span data-stu-id="be10f-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="be10f-129">O resultado corresponde de segunda (1) a domingo (7).</span><span class="sxs-lookup"><span data-stu-id="be10f-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="be10f-130">Não são feitos arredondamentos.</span><span class="sxs-lookup"><span data-stu-id="be10f-130">No rounding is done.</span></span> <span data-ttu-id="be10f-131">Se  _a data e_ a hora não puderem ser interpretadas como uma data ou hora válidas, a função retornará uma #VALUE!</span><span class="sxs-lookup"><span data-stu-id="be10f-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="be10f-132">.</span><span class="sxs-lookup"><span data-stu-id="be10f-132">error.</span></span> 
  
<span data-ttu-id="be10f-133">A função WEEKDAY também aceita um  valor de número único para a expressão em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="be10f-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="be10f-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be10f-134">Example 1</span></span>

<span data-ttu-id="be10f-135">WEEKDAY("30 de maio de 1999")</span><span class="sxs-lookup"><span data-stu-id="be10f-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="be10f-136">Retornará 7.</span><span class="sxs-lookup"><span data-stu-id="be10f-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="be10f-137">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="be10f-137">Example 2</span></span>

<span data-ttu-id="be10f-138">WEEKDAY(DATEVALUE("30 de maio de 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="be10f-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="be10f-139">Retornará 2.</span><span class="sxs-lookup"><span data-stu-id="be10f-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="be10f-140">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="be10f-140">Example 3</span></span>

<span data-ttu-id="be10f-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="be10f-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="be10f-142">Retornará 4.</span><span class="sxs-lookup"><span data-stu-id="be10f-142">Returns 4.</span></span>
  

