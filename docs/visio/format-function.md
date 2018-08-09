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
description: Retorna o resultado da expressão como uma cadeia de caracteres formatada de acordo com a figura de formatação.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771936"
---
# <a name="format-function"></a><span data-ttu-id="a3d9f-103">Função FORMAT</span><span class="sxs-lookup"><span data-stu-id="a3d9f-103">FORMAT Function</span></span>

<span data-ttu-id="a3d9f-104">Retorna o resultado da _expressão_ como uma cadeia de caracteres formatada de acordo com a _Figura de formatação_.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a3d9f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d9f-105">Syntax</span></span>

<span data-ttu-id="a3d9f-106">FORMATO (* * *expressão* * *, "* * *formatpicture* * *")</span><span class="sxs-lookup"><span data-stu-id="a3d9f-106">FORMAT(** *expression* **," ** *formatpicture* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a3d9f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d9f-107">Parameters</span></span>

|<span data-ttu-id="a3d9f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a3d9f-108">**Name**</span></span>|<span data-ttu-id="a3d9f-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a3d9f-109">**Required/Optional**</span></span>|<span data-ttu-id="a3d9f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a3d9f-110">**Data Type**</span></span>|<span data-ttu-id="a3d9f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a3d9f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3d9f-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="a3d9f-112">_expression_</span></span> <br/> |<span data-ttu-id="a3d9f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3d9f-113">Required</span></span>  <br/> |<span data-ttu-id="a3d9f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a3d9f-114">**String**</span></span> <br/> |<span data-ttu-id="a3d9f-115">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="a3d9f-116">_Figura de formatação_</span><span class="sxs-lookup"><span data-stu-id="a3d9f-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="a3d9f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3d9f-117">Required</span></span>  <br/> |<span data-ttu-id="a3d9f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a3d9f-118">**String**</span></span> <br/> |<span data-ttu-id="a3d9f-119">A imagem de formato usada para formatar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a3d9f-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a3d9f-120">Return value</span></span>

<span data-ttu-id="a3d9f-121">String</span><span class="sxs-lookup"><span data-stu-id="a3d9f-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3d9f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3d9f-122">Remarks</span></span>

<span data-ttu-id="a3d9f-123">O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="a3d9f-124">A _Figura de formatação_ deve ser apropriado para o tipo de expressão.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="a3d9f-125">Para obter mais informações sobre como especificar o formato de imagens, consulte [sobre figuras de formatação](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="a3d9f-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="a3d9f-126">Retorna um erro se o resultado de _expression_ e o tipo esperado em _formatpicture_ forem diferentes ou se há erros de sintaxe em _formatpicture_.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="a3d9f-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3d9f-127">Example 1</span></span>

<span data-ttu-id="a3d9f-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="a3d9f-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="a3d9f-129">Retornará 0,250 cm.</span><span class="sxs-lookup"><span data-stu-id="a3d9f-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a3d9f-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a3d9f-130">Example 2</span></span>

<span data-ttu-id="a3d9f-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="a3d9f-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="a3d9f-132">Returns "0,25 CM."</span><span class="sxs-lookup"><span data-stu-id="a3d9f-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a3d9f-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a3d9f-133">Example 3</span></span>

<span data-ttu-id="a3d9f-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="a3d9f-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="a3d9f-135">Returns "0,3 cm."</span><span class="sxs-lookup"><span data-stu-id="a3d9f-135">Returns "0.3 cm."</span></span>
  

