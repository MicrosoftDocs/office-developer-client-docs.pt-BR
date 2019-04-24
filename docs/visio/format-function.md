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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339890"
---
# <a name="format-function"></a><span data-ttu-id="ebffd-103">Função FORMAT</span><span class="sxs-lookup"><span data-stu-id="ebffd-103">FORMAT Function</span></span>

<span data-ttu-id="ebffd-104">Retorna o resultado da _expressão_ como uma cadeia de caracteres formatada de acordo com o _formatPicture_.</span><span class="sxs-lookup"><span data-stu-id="ebffd-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ebffd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebffd-105">Syntax</span></span>

<span data-ttu-id="ebffd-106">Formato (\* \* *expressão* \* *, "* \* *formatPicture* \* \*")</span><span class="sxs-lookup"><span data-stu-id="ebffd-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ebffd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebffd-107">Parameters</span></span>

|<span data-ttu-id="ebffd-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ebffd-108">**Name**</span></span>|<span data-ttu-id="ebffd-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ebffd-109">**Required/Optional**</span></span>|<span data-ttu-id="ebffd-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ebffd-110">**Data Type**</span></span>|<span data-ttu-id="ebffd-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ebffd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ebffd-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="ebffd-112">_expression_</span></span> <br/> |<span data-ttu-id="ebffd-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ebffd-113">Required</span></span>  <br/> |<span data-ttu-id="ebffd-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ebffd-114">**String**</span></span> <br/> |<span data-ttu-id="ebffd-115">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.</span><span class="sxs-lookup"><span data-stu-id="ebffd-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="ebffd-116">_formatPicture_</span><span class="sxs-lookup"><span data-stu-id="ebffd-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="ebffd-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ebffd-117">Required</span></span>  <br/> |<span data-ttu-id="ebffd-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ebffd-118">**String**</span></span> <br/> |<span data-ttu-id="ebffd-119">A imagem de formato usada para formatar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ebffd-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ebffd-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ebffd-120">Return value</span></span>

<span data-ttu-id="ebffd-121">String</span><span class="sxs-lookup"><span data-stu-id="ebffd-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebffd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebffd-122">Remarks</span></span>

<span data-ttu-id="ebffd-123">O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="ebffd-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="ebffd-124">O _formatPicture_ deve ser apropriado para o tipo de expressão.</span><span class="sxs-lookup"><span data-stu-id="ebffd-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="ebffd-125">Para obter mais informações sobre como especificar imagens de formato, consulte [about Format Pictures](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="ebffd-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="ebffd-126">Retorna um erro se o resultado da _expressão_ e o tipo esperado em _formatPicture_ forem de um tipo diferente ou se houver erros de sintaxe no _formatPicture_.</span><span class="sxs-lookup"><span data-stu-id="ebffd-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ebffd-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ebffd-127">Example 1</span></span>

<span data-ttu-id="ebffd-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="ebffd-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="ebffd-129">Retornará 0,250 cm.</span><span class="sxs-lookup"><span data-stu-id="ebffd-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ebffd-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ebffd-130">Example 2</span></span>

<span data-ttu-id="ebffd-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="ebffd-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="ebffd-132">Returns "0,25 CM."</span><span class="sxs-lookup"><span data-stu-id="ebffd-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ebffd-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ebffd-133">Example 3</span></span>

<span data-ttu-id="ebffd-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="ebffd-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="ebffd-135">Returns "0,3 cm."</span><span class="sxs-lookup"><span data-stu-id="ebffd-135">Returns "0.3 cm."</span></span>
  

