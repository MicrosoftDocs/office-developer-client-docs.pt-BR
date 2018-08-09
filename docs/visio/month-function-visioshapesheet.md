---
title: Função MONTH (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Retorna um inteiro de 1 a 12 que representa um mês.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772400"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="d90f7-103">Função MONTH (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d90f7-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d90f7-104">Retorna um inteiro de 1 a 12 que representa um mês.</span><span class="sxs-lookup"><span data-stu-id="d90f7-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d90f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d90f7-105">Syntax</span></span>

<span data-ttu-id="d90f7-106">MONTH ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="d90f7-106">MONTH(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d90f7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d90f7-107">Parameters</span></span>

|<span data-ttu-id="d90f7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d90f7-108">**Name**</span></span>|<span data-ttu-id="d90f7-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d90f7-109">**Required/Optional**</span></span>|<span data-ttu-id="d90f7-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d90f7-110">**Data Type**</span></span>|<span data-ttu-id="d90f7-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d90f7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d90f7-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="d90f7-112">_datetime_</span></span> <br/> |<span data-ttu-id="d90f7-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d90f7-113">Required</span></span>  <br/> |<span data-ttu-id="d90f7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d90f7-114">**String**</span></span> <br/> |<span data-ttu-id="d90f7-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="d90f7-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d90f7-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="d90f7-116">_expression_</span></span> <br/> |<span data-ttu-id="d90f7-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d90f7-117">Required</span></span>  <br/> |<span data-ttu-id="d90f7-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d90f7-118">**String**</span></span> <br/> | <span data-ttu-id="d90f7-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="d90f7-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d90f7-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d90f7-120">_lcid_</span></span> <br/> |<span data-ttu-id="d90f7-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="d90f7-121">Optional</span></span>  <br/> |<span data-ttu-id="d90f7-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="d90f7-122">**Number**</span></span> <br/> |<span data-ttu-id="d90f7-p101">O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="d90f7-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d90f7-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d90f7-125">Return value</span></span>

<span data-ttu-id="d90f7-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d90f7-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d90f7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d90f7-127">Remarks</span></span>

<span data-ttu-id="d90f7-128">O componente de hora de _datetime_ ou _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="d90f7-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d90f7-p102">Não é feito nenhum arredondamento. Se a cadeia de caracteres estiver faltando ou não puder ser convertida em um resultado válido, a função MONTH retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d90f7-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="d90f7-131">O valor retornado é formatado de acordo com o estilo de data curta definido pelas Configurações regionais atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="d90f7-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="d90f7-132">A função MONTH também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="d90f7-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d90f7-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d90f7-133">Example 1</span></span>

<span data-ttu-id="d90f7-134">MONTH("30 de maio de 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="d90f7-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="d90f7-135">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="d90f7-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d90f7-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d90f7-136">Example 2</span></span>

<span data-ttu-id="d90f7-137">MONTH(DATEVALUE("30 de maio de 1999")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="d90f7-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="d90f7-138">Retornará 6.</span><span class="sxs-lookup"><span data-stu-id="d90f7-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d90f7-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d90f7-139">Example 3</span></span>

<span data-ttu-id="d90f7-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="d90f7-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="d90f7-141">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="d90f7-141">Returns 5.</span></span>
  

