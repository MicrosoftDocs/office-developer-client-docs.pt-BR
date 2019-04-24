---
title: Função HOUR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Retorna um inteiro, de 0 a 23, representando a hora do dia de DateTime ou expressão.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329964"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="9965f-103">Função HOUR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="9965f-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="9965f-104">Retorna um inteiro, de 0 a 23, representando a hora do dia de _DateTime_ ou _expressão_.</span><span class="sxs-lookup"><span data-stu-id="9965f-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9965f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9965f-105">Syntax</span></span>

<span data-ttu-id="9965f-106">HOUR ("\* \* *DateTime* \* \*" | \* \* *expressão* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="9965f-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9965f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9965f-107">Parameters</span></span>

|<span data-ttu-id="9965f-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9965f-108">**Name**</span></span>|<span data-ttu-id="9965f-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="9965f-109">**Required/Optional**</span></span>|<span data-ttu-id="9965f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9965f-110">**Data Type**</span></span>|<span data-ttu-id="9965f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9965f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9965f-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="9965f-112">_datetime_</span></span> <br/> |<span data-ttu-id="9965f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9965f-113">Required</span></span>  <br/> |<span data-ttu-id="9965f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9965f-114">**String**</span></span> <br/> | <span data-ttu-id="9965f-115">Uma cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="9965f-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="9965f-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="9965f-116">_expression_</span></span> <br/> |<span data-ttu-id="9965f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9965f-117">Required</span></span>  <br/> |<span data-ttu-id="9965f-118">**Vai**</span><span class="sxs-lookup"><span data-stu-id="9965f-118">**Varies**</span></span> <br/> |<span data-ttu-id="9965f-119">Uma expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="9965f-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="9965f-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="9965f-120">_lcid_</span></span> <br/> |<span data-ttu-id="9965f-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="9965f-121">Optional</span></span>  <br/> |<span data-ttu-id="9965f-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="9965f-122">**Number**</span></span> <br/> | <span data-ttu-id="9965f-123">Um identificador de local a ser utilizado na avaliação de uma data e hora não-locais.</span><span class="sxs-lookup"><span data-stu-id="9965f-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="9965f-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="9965f-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9965f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9965f-125">Remarks</span></span>

<span data-ttu-id="9965f-126">O componente de data em *DateTime* e *expression* é Descartado.</span><span class="sxs-lookup"><span data-stu-id="9965f-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="9965f-127">Não é feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="9965f-127">No rounding is done.</span></span> <span data-ttu-id="9965f-128">Se o *DateTime* estiver faltando ou não puder ser convertido em um resultado válido, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9965f-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="9965f-129">O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="9965f-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="9965f-130">A função HOUR também aceita um valor de número único para *expressão* em que a parte decimal do resultado representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="9965f-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9965f-131">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9965f-131">Example 1</span></span>

<span data-ttu-id="9965f-132">HORA ("15:45")</span><span class="sxs-lookup"><span data-stu-id="9965f-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="9965f-133">Retornará 15.</span><span class="sxs-lookup"><span data-stu-id="9965f-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9965f-134">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9965f-134">Example 2</span></span>

<span data-ttu-id="9965f-135">HOUR("30 de maio de 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="9965f-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="9965f-136">Retornará 15.</span><span class="sxs-lookup"><span data-stu-id="9965f-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9965f-137">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9965f-137">Example 3</span></span>

<span data-ttu-id="9965f-138">HORA (0,5)</span><span class="sxs-lookup"><span data-stu-id="9965f-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="9965f-139">Retornará 12.</span><span class="sxs-lookup"><span data-stu-id="9965f-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="9965f-140">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="9965f-140">Example 4</span></span>

<span data-ttu-id="9965f-141">HORA ("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="9965f-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="9965f-142">Retornará 0.</span><span class="sxs-lookup"><span data-stu-id="9965f-142">Returns 0.</span></span>
  

