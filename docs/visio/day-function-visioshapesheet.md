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
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771690"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="da168-104">Função DAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="da168-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="da168-105">Retorna um número inteiro, de 1 a 31, representando o dia em _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="da168-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="da168-106">A função DAY usa o calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="da168-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="da168-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da168-107">Syntax</span></span>

<span data-ttu-id="da168-108">DIA ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="da168-108">DAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="da168-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da168-109">Parameters</span></span>

|<span data-ttu-id="da168-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="da168-110">**Name**</span></span>|<span data-ttu-id="da168-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="da168-111">**Required/Optional**</span></span>|<span data-ttu-id="da168-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="da168-112">**Data Type**</span></span>|<span data-ttu-id="da168-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="da168-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="da168-114">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="da168-114">_datetime_</span></span> <br/> |<span data-ttu-id="da168-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="da168-115">Required</span></span>  <br/> |<span data-ttu-id="da168-116">**String**</span><span class="sxs-lookup"><span data-stu-id="da168-116">**String**</span></span> <br/> |<span data-ttu-id="da168-117">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="da168-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="da168-118">_expressão_</span><span class="sxs-lookup"><span data-stu-id="da168-118">_expression_</span></span> <br/> |<span data-ttu-id="da168-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="da168-119">Required</span></span>  <br/> |<span data-ttu-id="da168-120">**String**</span><span class="sxs-lookup"><span data-stu-id="da168-120">**String**</span></span> <br/> |<span data-ttu-id="da168-121">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="da168-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="da168-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="da168-122">_lcid_</span></span> <br/> |<span data-ttu-id="da168-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="da168-123">Optional</span></span>  <br/> |<span data-ttu-id="da168-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="da168-124">**Number**</span></span> <br/> |<span data-ttu-id="da168-p103">Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="da168-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="da168-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="da168-127">Return value</span></span>

<span data-ttu-id="da168-128">Inteiro</span><span class="sxs-lookup"><span data-stu-id="da168-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da168-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="da168-129">Remarks</span></span>

<span data-ttu-id="da168-130">Qualquer componente de hora em _datetime_ ou _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="da168-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="da168-131">É feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="da168-131">No rounding is done.</span></span> <span data-ttu-id="da168-132">Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="da168-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="da168-133">A função DAY também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="da168-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="da168-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da168-134">Example 1</span></span>

<span data-ttu-id="da168-135">DAY("30 de maio de 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="da168-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="da168-136">Retornará 30.</span><span class="sxs-lookup"><span data-stu-id="da168-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="da168-137">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="da168-137">Example 2</span></span>

<span data-ttu-id="da168-138">DAY(DATEVALUE("30 de maio de 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="da168-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="da168-139">Retornará 6.</span><span class="sxs-lookup"><span data-stu-id="da168-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="da168-140">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="da168-140">Example 3</span></span>

<span data-ttu-id="da168-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="da168-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="da168-142">Retornará 30.</span><span class="sxs-lookup"><span data-stu-id="da168-142">Returns 30.</span></span>
  

