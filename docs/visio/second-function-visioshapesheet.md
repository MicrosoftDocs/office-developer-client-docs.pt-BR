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
description: Retorna um inteiro, de 0 a 59, que representa o componente de segundos de datetime ou expression.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772846"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="d7cf3-103">Função SECOND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d7cf3-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d7cf3-104">Retorna um inteiro, de 0 a 59, que representa o componente de segundos de _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d7cf3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7cf3-105">Syntax</span></span>

<span data-ttu-id="d7cf3-106">SEGUNDO ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="d7cf3-106">SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d7cf3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7cf3-107">Parameters</span></span>

|<span data-ttu-id="d7cf3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-108">**Name**</span></span>|<span data-ttu-id="d7cf3-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-109">**Required/Optional**</span></span>|<span data-ttu-id="d7cf3-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-110">**Data Type**</span></span>|<span data-ttu-id="d7cf3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d7cf3-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="d7cf3-112">_datetime_</span></span> <br/> |<span data-ttu-id="d7cf3-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d7cf3-113">Required</span></span>  <br/> |<span data-ttu-id="d7cf3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-114">**String**</span></span> <br/> |<span data-ttu-id="d7cf3-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d7cf3-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="d7cf3-116">_expression_</span></span> <br/> |<span data-ttu-id="d7cf3-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d7cf3-117">Required</span></span>  <br/> |<span data-ttu-id="d7cf3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-118">**String**</span></span> <br/> | <span data-ttu-id="d7cf3-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d7cf3-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d7cf3-120">_lcid_</span></span> <br/> |<span data-ttu-id="d7cf3-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="d7cf3-121">Optional</span></span>  <br/> |<span data-ttu-id="d7cf3-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="d7cf3-122">**Numeric**</span></span> <br/> |<span data-ttu-id="d7cf3-123">O identificador de localidade a ser usado ao avaliar um não- _datetime_.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="d7cf3-124">O identificador de localidade é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d7cf3-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d7cf3-125">Return value</span></span>

<span data-ttu-id="d7cf3-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d7cf3-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7cf3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7cf3-127">Remarks</span></span>

<span data-ttu-id="d7cf3-128">O componente de data em _datetime_ ou _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d7cf3-129">É feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-129">No rounding is done.</span></span> <span data-ttu-id="d7cf3-130">Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, essa função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="d7cf3-131">A função SECOND também aceita um valor de número único para _expression_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d7cf3-132">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7cf3-132">Example 1</span></span>

<span data-ttu-id="d7cf3-133">DATEVALUE("30/05/97 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="d7cf3-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="d7cf3-134">Retornará 32.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d7cf3-135">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d7cf3-135">Example 2</span></span>

<span data-ttu-id="d7cf3-136">SECOND(TIMEVALUE("30 de maio de 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="d7cf3-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="d7cf3-137">Retornará 52.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d7cf3-138">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d7cf3-138">Example 3</span></span>

<span data-ttu-id="d7cf3-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="d7cf3-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="d7cf3-140">Retornará 32.</span><span class="sxs-lookup"><span data-stu-id="d7cf3-140">Returns 32.</span></span>
  

