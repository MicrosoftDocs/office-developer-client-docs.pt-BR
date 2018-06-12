---
title: Função WEEKDAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Retorna um inteiro, de 1 a 7, que representa o dia da semana em datetime ou expression.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773281"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="960b5-103">Função WEEKDAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="960b5-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="960b5-104">Retorna um inteiro, de 1 a 7, que representa o dia da semana em _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="960b5-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="960b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="960b5-105">Syntax</span></span>

<span data-ttu-id="960b5-106">WEEKDAY ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="960b5-106">WEEKDAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="960b5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="960b5-107">Parameters</span></span>

|<span data-ttu-id="960b5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="960b5-108">**Name**</span></span>|<span data-ttu-id="960b5-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="960b5-109">**Required/Optional**</span></span>|<span data-ttu-id="960b5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="960b5-110">**Data Type**</span></span>|<span data-ttu-id="960b5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="960b5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="960b5-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="960b5-112">_datetime_</span></span> <br/> |<span data-ttu-id="960b5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="960b5-113">Required</span></span>  <br/> |<span data-ttu-id="960b5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="960b5-114">**String**</span></span> <br/> | <span data-ttu-id="960b5-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="960b5-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="960b5-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="960b5-116">_expression_</span></span> <br/> |<span data-ttu-id="960b5-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="960b5-117">Required</span></span>  <br/> |<span data-ttu-id="960b5-118">**Varia**</span><span class="sxs-lookup"><span data-stu-id="960b5-118">**Varies**</span></span> <br/> |<span data-ttu-id="960b5-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="960b5-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="960b5-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="960b5-120">_lcid_</span></span> <br/> |<span data-ttu-id="960b5-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="960b5-121">Optional</span></span>  <br/> |<span data-ttu-id="960b5-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="960b5-122">**Numeric**</span></span> <br/> |<span data-ttu-id="960b5-p101">O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="960b5-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="960b5-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="960b5-125">Return value</span></span>

<span data-ttu-id="960b5-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="960b5-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="960b5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="960b5-127">Remarks</span></span>

<span data-ttu-id="960b5-128">O componente de hora em _datetime_ ou _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="960b5-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="960b5-129">O resultado corresponde à segunda (1) a domingo (7).</span><span class="sxs-lookup"><span data-stu-id="960b5-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="960b5-130">É feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="960b5-130">No rounding is done.</span></span> <span data-ttu-id="960b5-131">Se _datetime_ estiver faltando ou não puder ser interpretada como uma data ou hora válida, a função retornará um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="960b5-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="960b5-132">erro.</span><span class="sxs-lookup"><span data-stu-id="960b5-132">error.</span></span> 
  
<span data-ttu-id="960b5-133">A função WEEKDAY também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="960b5-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="960b5-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="960b5-134">Example 1</span></span>

<span data-ttu-id="960b5-135">WEEKDAY("30 de maio de 1999")</span><span class="sxs-lookup"><span data-stu-id="960b5-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="960b5-136">Retornará 7.</span><span class="sxs-lookup"><span data-stu-id="960b5-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="960b5-137">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="960b5-137">Example 2</span></span>

<span data-ttu-id="960b5-138">WEEKDAY(DATEVALUE("30 de maio de 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="960b5-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="960b5-139">Retornará 2.</span><span class="sxs-lookup"><span data-stu-id="960b5-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="960b5-140">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="960b5-140">Example 3</span></span>

<span data-ttu-id="960b5-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="960b5-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="960b5-142">Retornará 4.</span><span class="sxs-lookup"><span data-stu-id="960b5-142">Returns 4.</span></span>
  

