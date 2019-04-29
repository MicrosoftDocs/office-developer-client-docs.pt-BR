---
title: Função FORMAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Retorna o resultado da expressão como uma cadeia de caracteres formatada de acordo com o formatPicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404649"
---
# <a name="format-function"></a><span data-ttu-id="2f560-103">Função FORMAT</span><span class="sxs-lookup"><span data-stu-id="2f560-103">FORMAT Function</span></span>

<span data-ttu-id="2f560-104">Retorna o resultado da _expressão_ como uma cadeia de caracteres formatada de acordo com o _formatPicture_.</span><span class="sxs-lookup"><span data-stu-id="2f560-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2f560-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f560-105">Syntax</span></span>

<span data-ttu-id="2f560-106">Formato (\* \* *expressão* \* *, "* \* *formatPicture* \* \*")</span><span class="sxs-lookup"><span data-stu-id="2f560-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2f560-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f560-107">Parameters</span></span>

|<span data-ttu-id="2f560-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2f560-108">**Name**</span></span>|<span data-ttu-id="2f560-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2f560-109">**Required/Optional**</span></span>|<span data-ttu-id="2f560-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2f560-110">**Data Type**</span></span>|<span data-ttu-id="2f560-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2f560-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2f560-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="2f560-112">_expression_</span></span> <br/> |<span data-ttu-id="2f560-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2f560-113">Required</span></span>  <br/> |<span data-ttu-id="2f560-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2f560-114">**String**</span></span> <br/> |<span data-ttu-id="2f560-115">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.</span><span class="sxs-lookup"><span data-stu-id="2f560-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="2f560-116">_formatPicture_</span><span class="sxs-lookup"><span data-stu-id="2f560-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="2f560-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2f560-117">Required</span></span>  <br/> |<span data-ttu-id="2f560-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2f560-118">**String**</span></span> <br/> |<span data-ttu-id="2f560-119">A imagem de formato usada para formatar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f560-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2f560-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2f560-120">Return value</span></span>

<span data-ttu-id="2f560-121">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="2f560-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f560-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f560-122">Remarks</span></span>

<span data-ttu-id="2f560-123">O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="2f560-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="2f560-124">O _formatPicture_ deve ser apropriado para o tipo de expressão.</span><span class="sxs-lookup"><span data-stu-id="2f560-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="2f560-125">Para obter mais informações sobre como especificar imagens de formato, consulte [about Format Pictures](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="2f560-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="2f560-126">Retorna um erro se o resultado da _expressão_ e o tipo esperado em _formatPicture_ forem de um tipo diferente ou se houver erros de sintaxe no _formatPicture_.</span><span class="sxs-lookup"><span data-stu-id="2f560-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="2f560-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f560-127">Example 1</span></span>

<span data-ttu-id="2f560-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="2f560-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="2f560-129">Retornará 0,250 cm.</span><span class="sxs-lookup"><span data-stu-id="2f560-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2f560-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2f560-130">Example 2</span></span>

<span data-ttu-id="2f560-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="2f560-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="2f560-132">Returns "0,25 CM."</span><span class="sxs-lookup"><span data-stu-id="2f560-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2f560-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2f560-133">Example 3</span></span>

<span data-ttu-id="2f560-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="2f560-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="2f560-135">Returns "0,3 cm."</span><span class="sxs-lookup"><span data-stu-id="2f560-135">Returns "0.3 cm."</span></span>
  

