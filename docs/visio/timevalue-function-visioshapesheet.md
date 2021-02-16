---
title: Função TIMEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Retorna o valor de hora representado por datetime ou expressão, com base nas configurações de Região e Idioma do sistema.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432321"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="4e42e-103">Função TIMEVALUE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4e42e-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4e42e-104">Retorna o valor de hora representado por  _datetime_ ou  _expressão,_ com base nas configurações de Região e Idioma do sistema.</span><span class="sxs-lookup"><span data-stu-id="4e42e-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4e42e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e42e-105">Syntax</span></span>

<span data-ttu-id="4e42e-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expressão* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="4e42e-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e42e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e42e-107">Parameters</span></span>

|<span data-ttu-id="4e42e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4e42e-108">**Name**</span></span>|<span data-ttu-id="4e42e-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="4e42e-109">**Required/Optional**</span></span>|<span data-ttu-id="4e42e-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4e42e-110">**Data Type**</span></span>|<span data-ttu-id="4e42e-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4e42e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e42e-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="4e42e-112">_datetime_</span></span> <br/> |<span data-ttu-id="4e42e-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4e42e-113">Required</span></span>  <br/> |<span data-ttu-id="4e42e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4e42e-114">**String**</span></span> <br/> | <span data-ttu-id="4e42e-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="4e42e-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="4e42e-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="4e42e-116">_expression_</span></span> <br/> |<span data-ttu-id="4e42e-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4e42e-117">Required</span></span>  <br/> |<span data-ttu-id="4e42e-118">**Varia**</span><span class="sxs-lookup"><span data-stu-id="4e42e-118">**Varies**</span></span> <br/> | <span data-ttu-id="4e42e-119">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="4e42e-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="4e42e-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="4e42e-120">_lcid_</span></span> <br/> |<span data-ttu-id="4e42e-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="4e42e-121">Optional</span></span>  <br/> |<span data-ttu-id="4e42e-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="4e42e-122">**Number**</span></span> <br/> |<span data-ttu-id="4e42e-123">O identificador de local a ser utilizado na avaliação de uma data e hora não locais.</span><span class="sxs-lookup"><span data-stu-id="4e42e-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="4e42e-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="4e42e-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e42e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e42e-125">Remarks</span></span>

<span data-ttu-id="4e42e-126">Qualquer componente de data ou hora  _na_ data  _ou expressão_ é descartado.</span><span class="sxs-lookup"><span data-stu-id="4e42e-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="4e42e-127">Se  _a data e_ a hora não puderem ser convertidas em um resultado válido, essa função retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4e42e-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="4e42e-128">.</span><span class="sxs-lookup"><span data-stu-id="4e42e-128">error.</span></span> 
  
<span data-ttu-id="4e42e-129">A função TIMEVALUE também aceita um  valor de número único para a expressão em que a parte decimal do resultado representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="4e42e-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4e42e-130">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e42e-130">Example 1</span></span>

<span data-ttu-id="4e42e-131">TIMEVALUE("6:00")</span><span class="sxs-lookup"><span data-stu-id="4e42e-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="4e42e-132">Retornará o valor que representa 06:00.</span><span class="sxs-lookup"><span data-stu-id="4e42e-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4e42e-133">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4e42e-133">Example 2</span></span>

<span data-ttu-id="4e42e-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="4e42e-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="4e42e-135">Retornará o valor que representa 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="4e42e-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4e42e-136">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4e42e-136">Example 3</span></span>

<span data-ttu-id="4e42e-137">TIMEVALUE("11:00, 1º de julho de 1997")</span><span class="sxs-lookup"><span data-stu-id="4e42e-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="4e42e-138">Retornará o valor que representa 11:00.</span><span class="sxs-lookup"><span data-stu-id="4e42e-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="4e42e-139">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4e42e-139">Example 4</span></span>

<span data-ttu-id="4e42e-140">TIMEVALUE(0,6337)</span><span class="sxs-lookup"><span data-stu-id="4e42e-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="4e42e-141">Retornará o valor que representa 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="4e42e-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="4e42e-142">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="4e42e-142">Example 5</span></span>

<span data-ttu-id="4e42e-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="4e42e-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="4e42e-p103">Retornará um erro de #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="4e42e-p103">Returns a #VALUE! error.</span></span>
  

