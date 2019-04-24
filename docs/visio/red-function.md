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
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359980"
---
# <a name="red-function"></a><span data-ttu-id="d3fcb-103">Função RED</span><span class="sxs-lookup"><span data-stu-id="d3fcb-103">RED Function</span></span>

<span data-ttu-id="d3fcb-104">Retorna o componente vermelho de uma cor.</span><span class="sxs-lookup"><span data-stu-id="d3fcb-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d3fcb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3fcb-105">Syntax</span></span>

<span data-ttu-id="d3fcb-106">VERMELHO (\* \* *expressão* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d3fcb-106">RED(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d3fcb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3fcb-107">Parameters</span></span>

|<span data-ttu-id="d3fcb-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d3fcb-108">**Name**</span></span>|<span data-ttu-id="d3fcb-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="d3fcb-109">**Required/Optional**</span></span>|<span data-ttu-id="d3fcb-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d3fcb-110">**Data Type**</span></span>|<span data-ttu-id="d3fcb-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d3fcb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d3fcb-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="d3fcb-112">_expression_</span></span> <br/> |<span data-ttu-id="d3fcb-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d3fcb-113">Required</span></span>  <br/> |<span data-ttu-id="d3fcb-114">**Vai**</span><span class="sxs-lookup"><span data-stu-id="d3fcb-114">**Varies**</span></span> <br/> |<span data-ttu-id="d3fcb-115">Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.</span><span class="sxs-lookup"><span data-stu-id="d3fcb-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d3fcb-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d3fcb-116">Return value</span></span>

<span data-ttu-id="d3fcb-117">Número</span><span class="sxs-lookup"><span data-stu-id="d3fcb-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3fcb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3fcb-118">Remarks</span></span>

<span data-ttu-id="d3fcb-119">O valor retornado é um número entre 0 e 255, inclusive, ou uma referência de célula que resulta em um índice.</span><span class="sxs-lookup"><span data-stu-id="d3fcb-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="d3fcb-120">Se a _expressão_ for inválida, esta função retornará 0 (preto).</span><span class="sxs-lookup"><span data-stu-id="d3fcb-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d3fcb-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3fcb-121">Example 1</span></span>

<span data-ttu-id="d3fcb-122">VERMELHO (22)</span><span class="sxs-lookup"><span data-stu-id="d3fcb-122">RED(22)</span></span>
  
<span data-ttu-id="d3fcb-123">Retornará 51 se o documento utilizar a paleta de cores padrão do Microsoft Office Visio, sendo cinza escuro a cor do índice 22.</span><span class="sxs-lookup"><span data-stu-id="d3fcb-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d3fcb-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d3fcb-124">Example 2</span></span>

<span data-ttu-id="d3fcb-125">VERMELHO (Char. Color)</span><span class="sxs-lookup"><span data-stu-id="d3fcb-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="d3fcb-126">Retorna o valor do componente vermelho da cor de origem atual.</span><span class="sxs-lookup"><span data-stu-id="d3fcb-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d3fcb-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d3fcb-127">Example 3</span></span>

<span data-ttu-id="d3fcb-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="d3fcb-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="d3fcb-129">Retornará 10.</span><span class="sxs-lookup"><span data-stu-id="d3fcb-129">Returns 10.</span></span>
  

