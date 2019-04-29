---
title: Função DATEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Retorna o valor de data representado por datetime ou expression.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360309"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="42eeb-103">Função DATEVALUE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="42eeb-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="42eeb-104">Retorna o valor de data representado por _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="42eeb-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="42eeb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42eeb-105">Syntax</span></span>

<span data-ttu-id="42eeb-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="42eeb-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="42eeb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42eeb-107">Parameters</span></span>

|<span data-ttu-id="42eeb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="42eeb-108">**Name**</span></span>|<span data-ttu-id="42eeb-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="42eeb-109">**Required/Optional**</span></span>|<span data-ttu-id="42eeb-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="42eeb-110">**Data Type**</span></span>|<span data-ttu-id="42eeb-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="42eeb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="42eeb-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="42eeb-112">_DateTime_</span></span> <br/> |<span data-ttu-id="42eeb-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="42eeb-113">Required</span></span>  <br/> |<span data-ttu-id="42eeb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="42eeb-114">**String**</span></span> <br/> |<span data-ttu-id="42eeb-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="42eeb-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="42eeb-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="42eeb-116">_expression_</span></span> <br/> |<span data-ttu-id="42eeb-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="42eeb-117">Required</span></span>  <br/> |<span data-ttu-id="42eeb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="42eeb-118">**String**</span></span> <br/> |<span data-ttu-id="42eeb-119">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="42eeb-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="42eeb-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="42eeb-120">_lcid_</span></span> <br/> |<span data-ttu-id="42eeb-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="42eeb-121">Optional</span></span>  <br/> |<span data-ttu-id="42eeb-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="42eeb-122">**Number**</span></span> <br/> |<span data-ttu-id="42eeb-p101">Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="42eeb-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="42eeb-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="42eeb-125">Return value</span></span>

<span data-ttu-id="42eeb-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="42eeb-126">DateTime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42eeb-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="42eeb-127">Remarks</span></span>

<span data-ttu-id="42eeb-128">Qualquer componente de tempo em *datetime* ou *expression* é descartado.</span><span class="sxs-lookup"><span data-stu-id="42eeb-128">Any time component in *datetime* or *expression* is discarded.</span></span> 
  
<span data-ttu-id="42eeb-129">Se a *datetime* estiver ausente ou não puder ser convertida em um resultado válido, DATEVALUE retornará um erro #VALUE!</span><span class="sxs-lookup"><span data-stu-id="42eeb-129">If *datetime* is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE! error.</span></span> <span data-ttu-id="42eeb-130">.</span><span class="sxs-lookup"><span data-stu-id="42eeb-130">error.</span></span> 
  
<span data-ttu-id="42eeb-131">O valor retornado é exibido usando o estilo de data abreviada definido pelas atuais configurações regionais do sistema.</span><span class="sxs-lookup"><span data-stu-id="42eeb-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="42eeb-132">A função DATEVALUE também aceita um valor de número único para *expression* em que a parte inteira do resultado representa os dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="42eeb-132">The DATEVALUE function also accepts a single number value for *expression* where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="42eeb-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42eeb-133">Example 1</span></span>

<span data-ttu-id="42eeb-134">DATEVALUE(AGORA( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="42eeb-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="42eeb-135">Retornará a data cinco dias a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="42eeb-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="42eeb-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="42eeb-136">Example 2</span></span>

<span data-ttu-id="42eeb-137">DATEVALUE("19/07/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="42eeb-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="42eeb-138">Retornará a data.</span><span class="sxs-lookup"><span data-stu-id="42eeb-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="42eeb-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="42eeb-139">Example 3</span></span>

<span data-ttu-id="42eeb-140">DATEVALUE("33 de maio de 1997")</span><span class="sxs-lookup"><span data-stu-id="42eeb-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="42eeb-p103">Retornar um erro #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="42eeb-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="42eeb-143">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="42eeb-143">Example 4</span></span>

<span data-ttu-id="42eeb-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="42eeb-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="42eeb-145">Retornará 30/5/1997.</span><span class="sxs-lookup"><span data-stu-id="42eeb-145">Returns 5/30/1997.</span></span>
  

