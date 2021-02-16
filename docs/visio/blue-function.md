---
title: Função BLUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Retorna o componente azul de uma cor. O valor de retorno é um inteiro no intervalo de 0 a 255, inclusive. A função retornará 0 para uma entrada inválida.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439034"
---
# <a name="blue-function"></a><span data-ttu-id="230d0-105">Função BLUE</span><span class="sxs-lookup"><span data-stu-id="230d0-105">BLUE Function</span></span>

<span data-ttu-id="230d0-106">Retorna o componente azul de uma cor.</span><span class="sxs-lookup"><span data-stu-id="230d0-106">Returns the blue component of a color.</span></span> <span data-ttu-id="230d0-107">O valor de retorno é um inteiro no intervalo de 0 a 255, inclusive.</span><span class="sxs-lookup"><span data-stu-id="230d0-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="230d0-108">A função retornará 0 para uma entrada inválida.</span><span class="sxs-lookup"><span data-stu-id="230d0-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="230d0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="230d0-109">Syntax</span></span>

<span data-ttu-id="230d0-110">Expressão BLUE(\*\*  \*\* )</span><span class="sxs-lookup"><span data-stu-id="230d0-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="230d0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="230d0-111">Parameters</span></span>

|<span data-ttu-id="230d0-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="230d0-112">**Name**</span></span>|<span data-ttu-id="230d0-113">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="230d0-113">**Required/Optional**</span></span>|<span data-ttu-id="230d0-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="230d0-114">**Data Type**</span></span>|<span data-ttu-id="230d0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="230d0-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="230d0-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="230d0-116">_expression_</span></span> <br/> |<span data-ttu-id="230d0-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="230d0-117">Required</span></span>  <br/> |<span data-ttu-id="230d0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="230d0-118">**String**</span></span> <br/> |<span data-ttu-id="230d0-119">Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.</span><span class="sxs-lookup"><span data-stu-id="230d0-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="230d0-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="230d0-120">Return value</span></span>

<span data-ttu-id="230d0-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="230d0-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="230d0-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="230d0-122">Example 1</span></span>

<span data-ttu-id="230d0-123">BLUE(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="230d0-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="230d0-124">Retornará o componente azul da cor de primeiro plano do preenchimento de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="230d0-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="230d0-125">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="230d0-125">Example 2</span></span>

<span data-ttu-id="230d0-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="230d0-126">BLUE(13)</span></span>
  
<span data-ttu-id="230d0-127">Retornará 128 se o documento utilizar a paleta de cores padrão do Visio, sendo ciano a cor do índice 13.</span><span class="sxs-lookup"><span data-stu-id="230d0-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="230d0-128">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="230d0-128">Example 3</span></span>

<span data-ttu-id="230d0-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="230d0-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="230d0-130">Retornará 30.</span><span class="sxs-lookup"><span data-stu-id="230d0-130">Returns 30.</span></span>
  

