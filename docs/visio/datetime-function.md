---
title: Função DATETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Retorna o valor de data e hora representado por datetime ou expression.
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771677"
---
# <a name="datetime-function"></a><span data-ttu-id="e9ee4-103">Função DATETIME</span><span class="sxs-lookup"><span data-stu-id="e9ee4-103">DATETIME Function</span></span>

<span data-ttu-id="e9ee4-104">Retorna o valor de data e hora representado por _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e9ee4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9ee4-105">Syntax</span></span>

<span data-ttu-id="e9ee4-106">DATETIME ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="e9ee4-106">DATETIME(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e9ee4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9ee4-107">Parameters</span></span>

|<span data-ttu-id="e9ee4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-108">**Name**</span></span>|<span data-ttu-id="e9ee4-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-109">**Required/Optional**</span></span>|<span data-ttu-id="e9ee4-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-110">**Data Type**</span></span>|<span data-ttu-id="e9ee4-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e9ee4-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="e9ee4-112">_datetime_</span></span> <br/> |<span data-ttu-id="e9ee4-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e9ee4-113">Required</span></span>  <br/> |<span data-ttu-id="e9ee4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-114">**String**</span></span> <br/> |<span data-ttu-id="e9ee4-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="e9ee4-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="e9ee4-116">_expression_</span></span> <br/> |<span data-ttu-id="e9ee4-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e9ee4-117">Required</span></span>  <br/> |<span data-ttu-id="e9ee4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-118">**String**</span></span> <br/> |<span data-ttu-id="e9ee4-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="e9ee4-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="e9ee4-120">_lcid_</span></span> <br/> |<span data-ttu-id="e9ee4-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="e9ee4-121">Optional</span></span>  <br/> |<span data-ttu-id="e9ee4-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="e9ee4-122">**Number**</span></span> <br/> |<span data-ttu-id="e9ee4-p101">Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e9ee4-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e9ee4-125">Return value</span></span>

<span data-ttu-id="e9ee4-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="e9ee4-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9ee4-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9ee4-127">Remarks</span></span>

<span data-ttu-id="e9ee4-128">Se *datetime* estiver faltando ou não puder ser interpretada como uma data ou hora válida, DATETIME retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="e9ee4-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="e9ee4-129">erro.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-129">error.</span></span> 
  
<span data-ttu-id="e9ee4-130">O valor retornado é formatado de acordo com o estilo de data e hora curtas nas Configurações regionais do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="e9ee4-131">A função DATETIME também aceita um valor de número único para *expression* em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899 e a parte decimal representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e9ee4-132">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9ee4-132">Example 1</span></span>

<span data-ttu-id="e9ee4-133">DATETIME("30 de maio de 1997")+5 ed.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="e9ee4-134">Retornará o valor que representa 04/06/97.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e9ee4-135">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e9ee4-135">Example 2</span></span>

<span data-ttu-id="e9ee4-136">FORMAT(DATETIME("20/05/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="e9ee4-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="e9ee4-137">Retornará a sequência de caracteres "Terça-feira, 20 de maio de 1997, 14:30:45."</span><span class="sxs-lookup"><span data-stu-id="e9ee4-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e9ee4-138">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e9ee4-138">Example 3</span></span>

<span data-ttu-id="e9ee4-139">DATETIME("13:30 19 de julho")</span><span class="sxs-lookup"><span data-stu-id="e9ee4-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="e9ee4-140">Retornará o valor que representa 19/07/2001 13:30 (partindo do pressuposto que o ano atual seja 2001).</span><span class="sxs-lookup"><span data-stu-id="e9ee4-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="e9ee4-141">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e9ee4-141">Example 4</span></span>

<span data-ttu-id="e9ee4-142">DATETIME(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="e9ee4-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="e9ee4-143">Retornará o valor representando 30/5/1997 3:12:32 PM.</span><span class="sxs-lookup"><span data-stu-id="e9ee4-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

