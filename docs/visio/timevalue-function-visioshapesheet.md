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
description: Retorna o valor de hora representado por datetime ou expressão, com base no idioma e região do sistema configurações.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773145"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="02b7a-103">Função TIMEVALUE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="02b7a-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="02b7a-104">Retorna o valor de hora representado por _datetime_ ou _expressão_, com base no idioma e região do sistema configurações.</span><span class="sxs-lookup"><span data-stu-id="02b7a-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="02b7a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02b7a-105">Syntax</span></span>

<span data-ttu-id="02b7a-106">TIMEVALUE ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="02b7a-106">TIMEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="02b7a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02b7a-107">Parameters</span></span>

|<span data-ttu-id="02b7a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="02b7a-108">**Name**</span></span>|<span data-ttu-id="02b7a-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="02b7a-109">**Required/Optional**</span></span>|<span data-ttu-id="02b7a-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="02b7a-110">**Data Type**</span></span>|<span data-ttu-id="02b7a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02b7a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="02b7a-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="02b7a-112">_datetime_</span></span> <br/> |<span data-ttu-id="02b7a-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02b7a-113">Required</span></span>  <br/> |<span data-ttu-id="02b7a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="02b7a-114">**String**</span></span> <br/> | <span data-ttu-id="02b7a-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="02b7a-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="02b7a-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="02b7a-116">_expression_</span></span> <br/> |<span data-ttu-id="02b7a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02b7a-117">Required</span></span>  <br/> |<span data-ttu-id="02b7a-118">**Varia**</span><span class="sxs-lookup"><span data-stu-id="02b7a-118">**Varies**</span></span> <br/> | <span data-ttu-id="02b7a-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="02b7a-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="02b7a-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="02b7a-120">_lcid_</span></span> <br/> |<span data-ttu-id="02b7a-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="02b7a-121">Optional</span></span>  <br/> |<span data-ttu-id="02b7a-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="02b7a-122">**Number**</span></span> <br/> |<span data-ttu-id="02b7a-p101">O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="02b7a-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02b7a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="02b7a-125">Remarks</span></span>

<span data-ttu-id="02b7a-126">Qualquer componente de data em _datetime_ ou _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="02b7a-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="02b7a-127">Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, essa função retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="02b7a-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="02b7a-128">erro.</span><span class="sxs-lookup"><span data-stu-id="02b7a-128">error.</span></span> 
  
<span data-ttu-id="02b7a-129">A função TIMEVALUE também aceita um valor de número único para _expression_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="02b7a-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="02b7a-130">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02b7a-130">Example 1</span></span>

<span data-ttu-id="02b7a-131">TIMEVALUE("6:00")</span><span class="sxs-lookup"><span data-stu-id="02b7a-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="02b7a-132">Retornará o valor que representa 06:00.</span><span class="sxs-lookup"><span data-stu-id="02b7a-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="02b7a-133">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="02b7a-133">Example 2</span></span>

<span data-ttu-id="02b7a-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="02b7a-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="02b7a-135">Retornará o valor que representa 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="02b7a-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="02b7a-136">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="02b7a-136">Example 3</span></span>

<span data-ttu-id="02b7a-137">TIMEVALUE("11:00, 1º de julho de 1997")</span><span class="sxs-lookup"><span data-stu-id="02b7a-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="02b7a-138">Retornará o valor que representa 11:00.</span><span class="sxs-lookup"><span data-stu-id="02b7a-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="02b7a-139">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="02b7a-139">Example 4</span></span>

<span data-ttu-id="02b7a-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="02b7a-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="02b7a-141">Retornará o valor que representa 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="02b7a-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="02b7a-142">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="02b7a-142">Example 5</span></span>

<span data-ttu-id="02b7a-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="02b7a-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="02b7a-p103">Retornará um erro de #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="02b7a-p103">Returns a #VALUE! error.</span></span>
  

