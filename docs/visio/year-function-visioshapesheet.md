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
description: Retorna um inteiro que representa o ano gregoriano em DateTime ou Expression, formatado de acordo com o estilo de data curta definido pelas configurações de região e idioma atuais do sistema.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420707"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="3d207-103">Função YEAR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3d207-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3d207-104">Retorna um inteiro que representa o ano gregoriano em _DateTime_ ou _expression_, formatado de acordo com o estilo de data curta definido pelas configurações de região e idioma atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="3d207-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3d207-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d207-105">Syntax</span></span>

<span data-ttu-id="3d207-106">YEAR ("\* \* *DateTime* \* \*" | \* \* *expressão* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="3d207-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3d207-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d207-107">Parameters</span></span>

|<span data-ttu-id="3d207-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3d207-108">**Name**</span></span>|<span data-ttu-id="3d207-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="3d207-109">**Required/Optional**</span></span>|<span data-ttu-id="3d207-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="3d207-110">**Data Type**</span></span>|<span data-ttu-id="3d207-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3d207-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3d207-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="3d207-112">_datetime_</span></span> <br/> |<span data-ttu-id="3d207-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3d207-113">Required</span></span>  <br/> |<span data-ttu-id="3d207-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3d207-114">**String**</span></span> <br/> | <span data-ttu-id="3d207-115">Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="3d207-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="3d207-116">_expressão_</span><span class="sxs-lookup"><span data-stu-id="3d207-116">_expression_</span></span> <br/> |<span data-ttu-id="3d207-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3d207-117">Required</span></span>  <br/> |<span data-ttu-id="3d207-118">**Vai**</span><span class="sxs-lookup"><span data-stu-id="3d207-118">**Varies**</span></span> <br/> |<span data-ttu-id="3d207-119">Qualquer expressão que produza uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="3d207-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="3d207-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="3d207-120">_lcid_</span></span> <br/> |<span data-ttu-id="3d207-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="3d207-121">Optional</span></span>  <br/> |<span data-ttu-id="3d207-122">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="3d207-122">**Numeric**</span></span> <br/> |<span data-ttu-id="3d207-123">O identificador de local a ser utilizado na avaliação de uma data e hora não locais.</span><span class="sxs-lookup"><span data-stu-id="3d207-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="3d207-124">O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="3d207-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3d207-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3d207-125">Return value</span></span>

<span data-ttu-id="3d207-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="3d207-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d207-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d207-127">Remarks</span></span>

<span data-ttu-id="3d207-128">O componente de hora em _DateTime_ ou _expression_ é Descartado.</span><span class="sxs-lookup"><span data-stu-id="3d207-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="3d207-129">Não é feito nenhum arredondamento.</span><span class="sxs-lookup"><span data-stu-id="3d207-129">No rounding is done.</span></span> <span data-ttu-id="3d207-130">Se _DateTime_ estiver ausente ou não puder ser interpretado como uma data ou hora válida, Year retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3d207-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="3d207-131">A função YEAR também aceita um valor de número único para _expressão_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899.</span><span class="sxs-lookup"><span data-stu-id="3d207-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3d207-132">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d207-132">Example 1</span></span>

<span data-ttu-id="3d207-133">YEAR ("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="3d207-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="3d207-134">Retornará 2007.</span><span class="sxs-lookup"><span data-stu-id="3d207-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3d207-135">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d207-135">Example 2</span></span>

<span data-ttu-id="3d207-136">YEAR(DATEVALUE("25 de dez de 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="3d207-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="3d207-137">Retornará 2007.</span><span class="sxs-lookup"><span data-stu-id="3d207-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3d207-138">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3d207-138">Example 3</span></span>

<span data-ttu-id="3d207-139">ANO (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="3d207-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="3d207-140">Retornará 1997.</span><span class="sxs-lookup"><span data-stu-id="3d207-140">Returns 1997.</span></span>
  

