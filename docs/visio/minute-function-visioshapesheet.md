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
description: Retorna um número inteiro entre 0 e 59 que representa o componente de minutos de datetime ou expression.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772397"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="83dde-103">Função MINUTE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="83dde-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="83dde-104">Retorna um número inteiro entre 0 e 59 que representa o componente de minutos de *datetime* ou *expression* .</span><span class="sxs-lookup"><span data-stu-id="83dde-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="83dde-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83dde-105">Syntax</span></span>

<span data-ttu-id="83dde-106">MINUTO (" *datetime* " |  *expressão*  [, *lcid* ])</span><span class="sxs-lookup"><span data-stu-id="83dde-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="83dde-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83dde-107">Parameters</span></span>

|<span data-ttu-id="83dde-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="83dde-108">**Name**</span></span>|<span data-ttu-id="83dde-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="83dde-109">**Required/Optional**</span></span>|<span data-ttu-id="83dde-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="83dde-110">**Data Type**</span></span>|<span data-ttu-id="83dde-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="83dde-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="83dde-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="83dde-112">_datetime_</span></span> <br/> |<span data-ttu-id="83dde-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="83dde-113">Required</span></span>  <br/> |<span data-ttu-id="83dde-114">**String**</span><span class="sxs-lookup"><span data-stu-id="83dde-114">**String**</span></span> <br/> |<span data-ttu-id="83dde-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="83dde-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="83dde-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="83dde-116">_expression_</span></span> <br/> |<span data-ttu-id="83dde-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="83dde-117">Required</span></span>  <br/> |<span data-ttu-id="83dde-118">**String**</span><span class="sxs-lookup"><span data-stu-id="83dde-118">**String**</span></span> <br/> | <span data-ttu-id="83dde-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="83dde-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="83dde-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="83dde-120">_lcid_</span></span> <br/> |<span data-ttu-id="83dde-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="83dde-121">Optional</span></span>  <br/> |<span data-ttu-id="83dde-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="83dde-122">**Number**</span></span> <br/> |<span data-ttu-id="83dde-p101">O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="83dde-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="83dde-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="83dde-125">Return value</span></span>

<span data-ttu-id="83dde-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="83dde-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83dde-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="83dde-127">Remarks</span></span>

<span data-ttu-id="83dde-128">O componente de data em _datetime_ e _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="83dde-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="83dde-129">É feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="83dde-129">No rounding is done.</span></span> <span data-ttu-id="83dde-130">Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="83dde-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="83dde-131">O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="83dde-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="83dde-132">A função MINUTE também aceita um valor de número único para _expression_ em que a parte decimal representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="83dde-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="83dde-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83dde-133">Example 1</span></span>

<span data-ttu-id="83dde-134">MINUTE("07/07/99 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="83dde-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="83dde-135">Retornará 45.</span><span class="sxs-lookup"><span data-stu-id="83dde-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="83dde-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="83dde-136">Example 2</span></span>

<span data-ttu-id="83dde-137">MINUTE(TIMEVALUE("25 de jan. de 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="83dde-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="83dde-138">Retornará 13.</span><span class="sxs-lookup"><span data-stu-id="83dde-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="83dde-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="83dde-139">Example 3</span></span>

<span data-ttu-id="83dde-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="83dde-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="83dde-141">Retornará 48.</span><span class="sxs-lookup"><span data-stu-id="83dde-141">Returns 48.</span></span>
  

