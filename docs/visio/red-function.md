---
title: Função RED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Retorna o componente vermelho de uma cor.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772638"
---
# <a name="red-function"></a><span data-ttu-id="85b02-103">Função RED</span><span class="sxs-lookup"><span data-stu-id="85b02-103">RED Function</span></span>

<span data-ttu-id="85b02-104">Retorna o componente vermelho de uma cor.</span><span class="sxs-lookup"><span data-stu-id="85b02-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="85b02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85b02-105">Syntax</span></span>

<span data-ttu-id="85b02-106">VERMELHO (* * *expressão* * *)</span><span class="sxs-lookup"><span data-stu-id="85b02-106">RED(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="85b02-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85b02-107">Parameters</span></span>

|<span data-ttu-id="85b02-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="85b02-108">**Name**</span></span>|<span data-ttu-id="85b02-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="85b02-109">**Required/Optional**</span></span>|<span data-ttu-id="85b02-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="85b02-110">**Data Type**</span></span>|<span data-ttu-id="85b02-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85b02-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="85b02-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="85b02-112">_expression_</span></span> <br/> |<span data-ttu-id="85b02-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="85b02-113">Required</span></span>  <br/> |<span data-ttu-id="85b02-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="85b02-114">**Varies**</span></span> <br/> |<span data-ttu-id="85b02-115">Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.</span><span class="sxs-lookup"><span data-stu-id="85b02-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="85b02-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="85b02-116">Return value</span></span>

<span data-ttu-id="85b02-117">Number</span><span class="sxs-lookup"><span data-stu-id="85b02-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85b02-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="85b02-118">Remarks</span></span>

<span data-ttu-id="85b02-119">O valor de retorno é um número no intervalo de 0 a 255, inclusive, ou uma referência de célula que resulta em um índice.</span><span class="sxs-lookup"><span data-stu-id="85b02-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="85b02-120">Se a _expressão_ for inválida, essa função retornará 0 (preto).</span><span class="sxs-lookup"><span data-stu-id="85b02-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="85b02-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85b02-121">Example 1</span></span>

<span data-ttu-id="85b02-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="85b02-122">RED(22)</span></span>
  
<span data-ttu-id="85b02-123">Retornará 51 se o documento utilizar a paleta de cores padrão do Microsoft Office Visio, sendo cinza escuro a cor do índice 22.</span><span class="sxs-lookup"><span data-stu-id="85b02-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="85b02-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="85b02-124">Example 2</span></span>

<span data-ttu-id="85b02-125">Red(char.Color)</span><span class="sxs-lookup"><span data-stu-id="85b02-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="85b02-126">Retorna o valor do componente vermelho da cor de origem atual.</span><span class="sxs-lookup"><span data-stu-id="85b02-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="85b02-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="85b02-127">Example 3</span></span>

<span data-ttu-id="85b02-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="85b02-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="85b02-129">Retornará 10.</span><span class="sxs-lookup"><span data-stu-id="85b02-129">Returns 10.</span></span>
  

