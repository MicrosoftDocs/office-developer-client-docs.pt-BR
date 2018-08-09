---
title: Função YEAR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Retorna um inteiro que representa o ano gregoriano em datetime ou expression, formatado de acordo com o estilo de data curta definido pelas configurações atuais de região e idioma do sistema.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773338"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="d349a-103">Função YEAR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d349a-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d349a-104">Retorna um inteiro que representa o ano gregoriano em _datetime_ ou _expressão_, formatado de acordo com o estilo de data curta definido pelas configurações atuais de região e idioma do sistema.</span><span class="sxs-lookup"><span data-stu-id="d349a-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d349a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d349a-105">Syntax</span></span>

<span data-ttu-id="d349a-106">ANO ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *])</span><span class="sxs-lookup"><span data-stu-id="d349a-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d349a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d349a-107">Parameters</span></span>

|<span data-ttu-id="d349a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d349a-108">**Name**</span></span>|<span data-ttu-id="d349a-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d349a-109">**Required/Optional**</span></span>|<span data-ttu-id="d349a-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d349a-110">**Data Type**</span></span>|<span data-ttu-id="d349a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d349a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d349a-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="d349a-112">_datetime_</span></span> <br/> |<span data-ttu-id="d349a-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d349a-113">Required</span></span>  <br/> |<span data-ttu-id="d349a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d349a-114">**String**</span></span> <br/> | <span data-ttu-id="d349a-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.</span><span class="sxs-lookup"><span data-stu-id="d349a-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d349a-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="d349a-116">_expression_</span></span> <br/> |<span data-ttu-id="d349a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d349a-117">Required</span></span>  <br/> |<span data-ttu-id="d349a-118">**Varia**</span><span class="sxs-lookup"><span data-stu-id="d349a-118">**Varies**</span></span> <br/> |<span data-ttu-id="d349a-119">Qualquer expressão que gere data e hora.</span><span class="sxs-lookup"><span data-stu-id="d349a-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d349a-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d349a-120">_lcid_</span></span> <br/> |<span data-ttu-id="d349a-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="d349a-121">Optional</span></span>  <br/> |<span data-ttu-id="d349a-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="d349a-122">**Numeric**</span></span> <br/> |<span data-ttu-id="d349a-p101">O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="d349a-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d349a-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d349a-125">Return value</span></span>

<span data-ttu-id="d349a-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d349a-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d349a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d349a-127">Remarks</span></span>

<span data-ttu-id="d349a-128">O componente de hora em _datetime_ ou _expression_ é desconsiderado.</span><span class="sxs-lookup"><span data-stu-id="d349a-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d349a-129">É feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="d349a-129">No rounding is done.</span></span> <span data-ttu-id="d349a-130">Se _datetime_ estiver faltando ou não puder ser interpretada como uma data ou hora válida, ano retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d349a-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="d349a-131">A função YEAR também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="d349a-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d349a-132">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d349a-132">Example 1</span></span>

<span data-ttu-id="d349a-133">YEAR("27/10/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="d349a-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="d349a-134">Retornará 2007.</span><span class="sxs-lookup"><span data-stu-id="d349a-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d349a-135">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d349a-135">Example 2</span></span>

<span data-ttu-id="d349a-136">YEAR(DATEVALUE("25 de dez de 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="d349a-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="d349a-137">Retornará 2007.</span><span class="sxs-lookup"><span data-stu-id="d349a-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d349a-138">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d349a-138">Example 3</span></span>

<span data-ttu-id="d349a-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="d349a-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="d349a-140">Retornará 1997.</span><span class="sxs-lookup"><span data-stu-id="d349a-140">Returns 1997.</span></span>
  

