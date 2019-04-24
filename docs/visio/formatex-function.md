---
title: Função FORMATEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Retorna o resultado da expressão avaliada em srcUnit como uma cadeia de caracteres formatada de acordo com o formato expresso no dstUnit.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328627"
---
# <a name="formatex-function"></a><span data-ttu-id="1e930-103">Função FORMATEX</span><span class="sxs-lookup"><span data-stu-id="1e930-103">FORMATEX Function</span></span>

<span data-ttu-id="1e930-104">Retorna o resultado da expressão avaliada em srcUnit como uma cadeia de caracteres formatada de acordo com o formato expresso no dstUnit.</span><span class="sxs-lookup"><span data-stu-id="1e930-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1e930-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e930-105">Syntax</span></span>

<span data-ttu-id="1e930-106">FORMATEX (\* \* *expressão* \* *, "* \* *formato* \* *", [* \* *srcUnit* \* *], [* \* *dstUnit* \* *], [* \* *LangID* \* \*] [, \* \* *calID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="1e930-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e930-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e930-107">Parameters</span></span>

|<span data-ttu-id="1e930-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1e930-108">**Name**</span></span>|<span data-ttu-id="1e930-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="1e930-109">**Required/Optional**</span></span>|<span data-ttu-id="1e930-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1e930-110">**Data Type**</span></span>|<span data-ttu-id="1e930-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1e930-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e930-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="1e930-112">_expression_</span></span> <br/> |<span data-ttu-id="1e930-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e930-113">Required</span></span>  <br/> |<span data-ttu-id="1e930-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1e930-114">**String**</span></span> <br/> |<span data-ttu-id="1e930-115">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.</span><span class="sxs-lookup"><span data-stu-id="1e930-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="1e930-116">_format_</span><span class="sxs-lookup"><span data-stu-id="1e930-116">_format_</span></span> <br/> |<span data-ttu-id="1e930-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e930-117">Required</span></span>  <br/> |<span data-ttu-id="1e930-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1e930-118">**String**</span></span> <br/> |<span data-ttu-id="1e930-119">A imagem de formato usada para formatar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1e930-119">The format picture used to format the string.</span></span> <span data-ttu-id="1e930-120">Para obter mais informações sobre como formatar imagens, consulte [about Format Pictures](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="1e930-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="1e930-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="1e930-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="1e930-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="1e930-122">Optional</span></span>  <br/> |<span data-ttu-id="1e930-123">**String**</span><span class="sxs-lookup"><span data-stu-id="1e930-123">**String**</span></span> <br/> | <span data-ttu-id="1e930-124">Unidades usadas para avaliar a expression (pol, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="1e930-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="1e930-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="1e930-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="1e930-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="1e930-126">Optional</span></span>  <br/> |<span data-ttu-id="1e930-127">**String**</span><span class="sxs-lookup"><span data-stu-id="1e930-127">**String**</span></span> <br/> |<span data-ttu-id="1e930-128">Unidades usadas para o resultado de expression (pol, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="1e930-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="1e930-129">_Lang_</span><span class="sxs-lookup"><span data-stu-id="1e930-129">_langID_</span></span> <br/> |<span data-ttu-id="1e930-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="1e930-130">Optional</span></span>  <br/> |<span data-ttu-id="1e930-131">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e930-131">**Number**</span></span> <br/> |<span data-ttu-id="1e930-132">O idioma usado ao formatar as imagens de data/hora do Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="1e930-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="1e930-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="1e930-133">_calID_</span></span> <br/> |<span data-ttu-id="1e930-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="1e930-134">Optional</span></span>  <br/> |<span data-ttu-id="1e930-135">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e930-135">**Number**</span></span> <br/> |<span data-ttu-id="1e930-136">O calendário usado ao formatar as imagens de data/hora do Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="1e930-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1e930-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1e930-137">Return value</span></span>

<span data-ttu-id="1e930-138">String</span><span class="sxs-lookup"><span data-stu-id="1e930-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e930-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e930-139">Remarks</span></span>

<span data-ttu-id="1e930-140">O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="1e930-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="1e930-141">O format deve ser adequado para o texto da expressão.</span><span class="sxs-lookup"><span data-stu-id="1e930-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="1e930-142">O argumento srcUnit é usado para dimensionar resultados de expressão não digitada, como 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="1e930-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="1e930-143">Se o resultado de expression possuir um texto explícito, como 3 pés + 8 pés, então srcUnit será ignorada.</span><span class="sxs-lookup"><span data-stu-id="1e930-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="1e930-144">O argumento dstUnit é usado para especificar as unidades usadas para o resultado formatado.</span><span class="sxs-lookup"><span data-stu-id="1e930-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="1e930-145">Se dstUnit não for especificado, as unidades para o resultado da expressão serão usadas.</span><span class="sxs-lookup"><span data-stu-id="1e930-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="1e930-146">Retorna um erro se o resultado de expression e o texto esperado em format forem de um tipo diferente, se houver erros de sintaxe em format ou se as unidades srcUnit ou dstUnit não forem reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="1e930-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="1e930-147">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1e930-147">Example</span></span>

<span data-ttu-id="1e930-148">FORMATEX(5,5, "0,00 u", "cm", "pés")</span><span class="sxs-lookup"><span data-stu-id="1e930-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="1e930-149">Retorna 0,18 pés.</span><span class="sxs-lookup"><span data-stu-id="1e930-149">Returns 0.18 feet.</span></span> 
  

