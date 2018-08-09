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
description: Retorna um número inteiro, de 0 a 23, representando a hora do dia de datetime ou expression.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772031"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="1e318-103">Função HOUR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="1e318-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="1e318-104">Retorna um número inteiro, de 0 a 23, representando a hora do dia de _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="1e318-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1e318-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e318-105">Syntax</span></span>

<span data-ttu-id="1e318-106">HORA ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="1e318-106">HOUR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e318-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e318-107">Parameters</span></span>

|<span data-ttu-id="1e318-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1e318-108">**Name**</span></span>|<span data-ttu-id="1e318-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1e318-109">**Required/Optional**</span></span>|<span data-ttu-id="1e318-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1e318-110">**Data Type**</span></span>|<span data-ttu-id="1e318-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1e318-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e318-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="1e318-112">_datetime_</span></span> <br/> |<span data-ttu-id="1e318-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e318-113">Required</span></span>  <br/> |<span data-ttu-id="1e318-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1e318-114">**String**</span></span> <br/> | <span data-ttu-id="1e318-115">Uma cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="1e318-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="1e318-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="1e318-116">_expression_</span></span> <br/> |<span data-ttu-id="1e318-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e318-117">Required</span></span>  <br/> |<span data-ttu-id="1e318-118">**Varia**</span><span class="sxs-lookup"><span data-stu-id="1e318-118">**Varies**</span></span> <br/> |<span data-ttu-id="1e318-119">Uma expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="1e318-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="1e318-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="1e318-120">_lcid_</span></span> <br/> |<span data-ttu-id="1e318-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="1e318-121">Optional</span></span>  <br/> |<span data-ttu-id="1e318-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e318-122">**Number**</span></span> <br/> | <span data-ttu-id="1e318-p101">Um identificador de local a ser utilizado na avaliação de uma data e hora não-locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="1e318-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e318-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e318-125">Remarks</span></span>

<span data-ttu-id="1e318-126">O componente de data em *datetime* e *expression* é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="1e318-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="1e318-127">É feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="1e318-127">No rounding is done.</span></span> <span data-ttu-id="1e318-128">Se a *datetime* estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1e318-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="1e318-129">O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="1e318-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="1e318-130">A função HOUR também aceita um valor de número único para *expression* em que a parte decimal do resultado representa a fração de um dia desde a meia-noite.</span><span class="sxs-lookup"><span data-stu-id="1e318-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1e318-131">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e318-131">Example 1</span></span>

<span data-ttu-id="1e318-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="1e318-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="1e318-133">Retornará 15.</span><span class="sxs-lookup"><span data-stu-id="1e318-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1e318-134">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1e318-134">Example 2</span></span>

<span data-ttu-id="1e318-135">HOUR("30 de maio de 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="1e318-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="1e318-136">Retornará 15.</span><span class="sxs-lookup"><span data-stu-id="1e318-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1e318-137">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1e318-137">Example 3</span></span>

<span data-ttu-id="1e318-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="1e318-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="1e318-139">Retornará 12.</span><span class="sxs-lookup"><span data-stu-id="1e318-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="1e318-140">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="1e318-140">Example 4</span></span>

<span data-ttu-id="1e318-141">HOUR("30/05/1997")</span><span class="sxs-lookup"><span data-stu-id="1e318-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="1e318-142">Retornará 0.</span><span class="sxs-lookup"><span data-stu-id="1e318-142">Returns 0.</span></span>
  

