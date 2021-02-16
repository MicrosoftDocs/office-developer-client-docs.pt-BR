---
title: Função MONTH (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Retorna um inteiro de 1 a 12 que representa um mês.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431971"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="63065-103">Função MONTH (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="63065-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="63065-104">Retorna um inteiro de 1 a 12 que representa um mês.</span><span class="sxs-lookup"><span data-stu-id="63065-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="63065-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63065-105">Syntax</span></span>

<span data-ttu-id="63065-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expressão* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="63065-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="63065-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63065-107">Parameters</span></span>

|<span data-ttu-id="63065-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="63065-108">**Name**</span></span>|<span data-ttu-id="63065-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="63065-109">**Required/Optional**</span></span>|<span data-ttu-id="63065-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="63065-110">**Data Type**</span></span>|<span data-ttu-id="63065-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="63065-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="63065-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="63065-112">_datetime_</span></span> <br/> |<span data-ttu-id="63065-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="63065-113">Required</span></span>  <br/> |<span data-ttu-id="63065-114">**String**</span><span class="sxs-lookup"><span data-stu-id="63065-114">**String**</span></span> <br/> |<span data-ttu-id="63065-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="63065-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="63065-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="63065-116">_expression_</span></span> <br/> |<span data-ttu-id="63065-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="63065-117">Required</span></span>  <br/> |<span data-ttu-id="63065-118">**String**</span><span class="sxs-lookup"><span data-stu-id="63065-118">**String**</span></span> <br/> | <span data-ttu-id="63065-119">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="63065-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="63065-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="63065-120">_lcid_</span></span> <br/> |<span data-ttu-id="63065-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="63065-121">Optional</span></span>  <br/> |<span data-ttu-id="63065-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="63065-122">**Number**</span></span> <br/> |<span data-ttu-id="63065-123">O identificador de local a ser utilizado na avaliação de uma data e hora não locais.</span><span class="sxs-lookup"><span data-stu-id="63065-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="63065-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="63065-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="63065-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63065-125">Return value</span></span>

<span data-ttu-id="63065-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="63065-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63065-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="63065-127">Remarks</span></span>

<span data-ttu-id="63065-128">O componente de hora  _da data e_ hora ou  _expressão_ é descartado.</span><span class="sxs-lookup"><span data-stu-id="63065-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="63065-p102">Não é feito nenhum arredondamento. Se a cadeia de caracteres estiver faltando ou não puder ser convertida em um resultado válido, a função MONTH retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="63065-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="63065-131">O valor retornado é formatado de acordo com o estilo de data curta definido pelas Configurações regionais atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="63065-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="63065-132">A função MONTH também aceita um  valor de número único para a expressão em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="63065-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="63065-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63065-133">Example 1</span></span>

<span data-ttu-id="63065-134">MONTH("30 de maio de 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="63065-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="63065-135">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="63065-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="63065-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="63065-136">Example 2</span></span>

<span data-ttu-id="63065-137">MONTH(DATEVALUE("30 de maio de 1999")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="63065-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="63065-138">Retornará 6.</span><span class="sxs-lookup"><span data-stu-id="63065-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="63065-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="63065-139">Example 3</span></span>

<span data-ttu-id="63065-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="63065-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="63065-141">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="63065-141">Returns 5.</span></span>
  

