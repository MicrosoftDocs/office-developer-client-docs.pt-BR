---
title: Função MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Retorna um inteiro de 0 a 59 que representa o componente de minutos de DateTime ou expressão.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283969"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="c243b-103">Função MINUTE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c243b-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c243b-104">Retorna um inteiro de 0 a 59 que representa o componente de minutos de *DateTime* ou *expressão* .</span><span class="sxs-lookup"><span data-stu-id="c243b-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c243b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c243b-105">Syntax</span></span>

<span data-ttu-id="c243b-106">MINUTE (" *DateTime* " |  *expressão*  [, *LCID* ])</span><span class="sxs-lookup"><span data-stu-id="c243b-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c243b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c243b-107">Parameters</span></span>

|<span data-ttu-id="c243b-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c243b-108">**Name**</span></span>|<span data-ttu-id="c243b-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="c243b-109">**Required/Optional**</span></span>|<span data-ttu-id="c243b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c243b-110">**Data Type**</span></span>|<span data-ttu-id="c243b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c243b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c243b-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="c243b-112">_datetime_</span></span> <br/> |<span data-ttu-id="c243b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c243b-113">Required</span></span>  <br/> |<span data-ttu-id="c243b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c243b-114">**String**</span></span> <br/> |<span data-ttu-id="c243b-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="c243b-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="c243b-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="c243b-116">_expression_</span></span> <br/> |<span data-ttu-id="c243b-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c243b-117">Required</span></span>  <br/> |<span data-ttu-id="c243b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c243b-118">**String**</span></span> <br/> | <span data-ttu-id="c243b-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="c243b-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="c243b-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="c243b-120">_lcid_</span></span> <br/> |<span data-ttu-id="c243b-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="c243b-121">Optional</span></span>  <br/> |<span data-ttu-id="c243b-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="c243b-122">**Number**</span></span> <br/> |<span data-ttu-id="c243b-123">O identificador de local a ser utilizado na avaliação de uma data e hora não locais.</span><span class="sxs-lookup"><span data-stu-id="c243b-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="c243b-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="c243b-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c243b-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c243b-125">Return value</span></span>

<span data-ttu-id="c243b-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c243b-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c243b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c243b-127">Remarks</span></span>

<span data-ttu-id="c243b-128">O componente de data em _DateTime_ e _expression_ é Descartado.</span><span class="sxs-lookup"><span data-stu-id="c243b-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="c243b-129">Não é feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="c243b-129">No rounding is done.</span></span> <span data-ttu-id="c243b-130">Se a _data/hora_ estiver ausente ou não puder ser convertida em um resultado válido, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c243b-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="c243b-131">O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="c243b-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="c243b-132">A função MINUTE também aceita um valor de número único para _expressão_ em que a parte decimal representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="c243b-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c243b-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c243b-133">Example 1</span></span>

<span data-ttu-id="c243b-134">MINUTE ("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="c243b-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="c243b-135">Retornará 45.</span><span class="sxs-lookup"><span data-stu-id="c243b-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c243b-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c243b-136">Example 2</span></span>

<span data-ttu-id="c243b-137">MINUTE(TIMEVALUE("25 de jan. de 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="c243b-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="c243b-138">Retornará 13.</span><span class="sxs-lookup"><span data-stu-id="c243b-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c243b-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c243b-139">Example 3</span></span>

<span data-ttu-id="c243b-140">MINUTE (0.575)</span><span class="sxs-lookup"><span data-stu-id="c243b-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="c243b-141">Retornará 48.</span><span class="sxs-lookup"><span data-stu-id="c243b-141">Returns 48.</span></span>
  

