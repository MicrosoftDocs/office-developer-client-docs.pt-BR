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
description: Retorna o resultado da expressão avaliado na UnOrigem como uma cadeia de caracteres formatada de acordo com o formato expressado na UnDestino.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771938"
---
# <a name="formatex-function"></a><span data-ttu-id="609b2-103">Função FORMATEX</span><span class="sxs-lookup"><span data-stu-id="609b2-103">FORMATEX Function</span></span>

<span data-ttu-id="609b2-104">Retorna o resultado da expressão avaliado na UnOrigem como uma cadeia de caracteres formatada de acordo com o formato expressado na UnDestino.</span><span class="sxs-lookup"><span data-stu-id="609b2-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="609b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="609b2-105">Syntax</span></span>

<span data-ttu-id="609b2-106">FORMATEX (* * *expressão* * *, "* * *formato* * *", [* * *UnOrigem* * *], [* * *UnDestino* * *], [* * *langID* * *] [, * * *calID* * *])</span><span class="sxs-lookup"><span data-stu-id="609b2-106">FORMATEX(** *expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="609b2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="609b2-107">Parameters</span></span>

|<span data-ttu-id="609b2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="609b2-108">**Name**</span></span>|<span data-ttu-id="609b2-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="609b2-109">**Required/Optional**</span></span>|<span data-ttu-id="609b2-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="609b2-110">**Data Type**</span></span>|<span data-ttu-id="609b2-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="609b2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="609b2-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="609b2-112">_expression_</span></span> <br/> |<span data-ttu-id="609b2-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="609b2-113">Required</span></span>  <br/> |<span data-ttu-id="609b2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="609b2-114">**String**</span></span> <br/> |<span data-ttu-id="609b2-115">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.</span><span class="sxs-lookup"><span data-stu-id="609b2-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="609b2-116">_format_</span><span class="sxs-lookup"><span data-stu-id="609b2-116">_format_</span></span> <br/> |<span data-ttu-id="609b2-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="609b2-117">Required</span></span>  <br/> |<span data-ttu-id="609b2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="609b2-118">**String**</span></span> <br/> |<span data-ttu-id="609b2-119">A figura de formatação usada para formatar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="609b2-119">The format picture used to format the string.</span></span> <span data-ttu-id="609b2-120">Para obter mais informações sobre figuras de formatação, consulte [Sobre figuras de formatação](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="609b2-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="609b2-121">_UnOrigem_</span><span class="sxs-lookup"><span data-stu-id="609b2-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="609b2-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="609b2-122">Optional</span></span>  <br/> |<span data-ttu-id="609b2-123">**String**</span><span class="sxs-lookup"><span data-stu-id="609b2-123">**String**</span></span> <br/> | <span data-ttu-id="609b2-124">Unidades usadas para avaliar a expression (pol, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="609b2-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="609b2-125">_UnDestino_</span><span class="sxs-lookup"><span data-stu-id="609b2-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="609b2-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="609b2-126">Optional</span></span>  <br/> |<span data-ttu-id="609b2-127">**String**</span><span class="sxs-lookup"><span data-stu-id="609b2-127">**String**</span></span> <br/> |<span data-ttu-id="609b2-128">Unidades usadas para o resultado de expression (pol, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="609b2-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="609b2-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="609b2-129">_langID_</span></span> <br/> |<span data-ttu-id="609b2-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="609b2-130">Optional</span></span>  <br/> |<span data-ttu-id="609b2-131">**Número**</span><span class="sxs-lookup"><span data-stu-id="609b2-131">**Number**</span></span> <br/> |<span data-ttu-id="609b2-132">O idioma usado ao formatar as imagens de data/hora do Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="609b2-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="609b2-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="609b2-133">_calID_</span></span> <br/> |<span data-ttu-id="609b2-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="609b2-134">Optional</span></span>  <br/> |<span data-ttu-id="609b2-135">**Número**</span><span class="sxs-lookup"><span data-stu-id="609b2-135">**Number**</span></span> <br/> |<span data-ttu-id="609b2-136">O calendário usado ao formatar as imagens de data/hora do Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="609b2-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="609b2-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="609b2-137">Return value</span></span>

<span data-ttu-id="609b2-138">String</span><span class="sxs-lookup"><span data-stu-id="609b2-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="609b2-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="609b2-139">Remarks</span></span>

<span data-ttu-id="609b2-p102">O texto da expressão e o texto especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada. O format deve ser adequado para o texto da expressão.</span><span class="sxs-lookup"><span data-stu-id="609b2-p102">The type of the expression and the type specified in the format picture govern the behavior of the returned string. The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="609b2-p103">O argumento srcUnit é usado para dimensionar resultados de expressão não digitada, como 3 + 4. Se o resultado de expression possuir um texto explícito, como 3 pés + 8 pés, então srcUnit será ignorada.</span><span class="sxs-lookup"><span data-stu-id="609b2-p103">The srcUnit argument is used to scale untyped expression results, such as 3 + 4. If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="609b2-p104">O argumento dstUnit é usado para especificar as unidades usadas para o resultado formatado. Se dstUnit não for especificado, as unidades para o resultado da expressão serão usadas.</span><span class="sxs-lookup"><span data-stu-id="609b2-p104">The dstUnit argument is used to specify the units used for the formatted result. If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="609b2-146">Retorna um erro se o resultado de expression e o texto esperado em format forem de um tipo diferente, se houver erros de sintaxe em format ou se as unidades srcUnit ou dstUnit não forem reconhecidas.</span><span class="sxs-lookup"><span data-stu-id="609b2-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="609b2-147">Exemplo</span><span class="sxs-lookup"><span data-stu-id="609b2-147">Example</span></span>

<span data-ttu-id="609b2-148">FORMATEX(5,5, "0,00 u", "cm", "pés")</span><span class="sxs-lookup"><span data-stu-id="609b2-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="609b2-149">Retorna 0,18 pés.</span><span class="sxs-lookup"><span data-stu-id="609b2-149">Returns 0.18 feet.</span></span> 
  
