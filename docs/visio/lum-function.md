---
title: Função LUM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Retorna o valor do componente de luminosidade de uma cor.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419335"
---
# <a name="lum-function"></a><span data-ttu-id="ea83f-103">Função LUM</span><span class="sxs-lookup"><span data-stu-id="ea83f-103">LUM Function</span></span>

<span data-ttu-id="ea83f-104">Retorna o valor do componente de luminosidade de uma cor.</span><span class="sxs-lookup"><span data-stu-id="ea83f-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ea83f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea83f-105">Syntax</span></span>

<span data-ttu-id="ea83f-106">Expressão LUM(\*\*  \*\* )</span><span class="sxs-lookup"><span data-stu-id="ea83f-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ea83f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea83f-107">Parameters</span></span>

|<span data-ttu-id="ea83f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea83f-108">**Name**</span></span>|<span data-ttu-id="ea83f-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ea83f-109">**Required/Optional**</span></span>|<span data-ttu-id="ea83f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ea83f-110">**Data Type**</span></span>|<span data-ttu-id="ea83f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ea83f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ea83f-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ea83f-112">_expression_</span></span> <br/> |<span data-ttu-id="ea83f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ea83f-113">Required</span></span>  <br/> |<span data-ttu-id="ea83f-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="ea83f-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ea83f-115">O índice de uma cor na tabela de cores do documento ou uma referência a uma célula que contenha um índice de cores.</span><span class="sxs-lookup"><span data-stu-id="ea83f-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ea83f-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ea83f-116">Return value</span></span>

<span data-ttu-id="ea83f-117">Número</span><span class="sxs-lookup"><span data-stu-id="ea83f-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea83f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea83f-118">Remarks</span></span>

<span data-ttu-id="ea83f-p101">O valor retornado é um número no intervalo de 0 a 240, inclusive. A função retornará 0 para uma entrada inválida.</span><span class="sxs-lookup"><span data-stu-id="ea83f-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ea83f-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea83f-121">Example 1</span></span>

<span data-ttu-id="ea83f-122">LUM(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="ea83f-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ea83f-123">Retornará a luminosidade da cor de preenchimento de primeiro plano de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="ea83f-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ea83f-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea83f-124">Example 2</span></span>

<span data-ttu-id="ea83f-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="ea83f-125">LUM(6)</span></span>
  
<span data-ttu-id="ea83f-126">Retornará 120 se o documento utilizar a paleta de cores padrão do Visio, sendo magenta a cor do índice 6.</span><span class="sxs-lookup"><span data-stu-id="ea83f-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ea83f-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ea83f-127">Example 3</span></span>

<span data-ttu-id="ea83f-128">LUM(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ea83f-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="ea83f-129">Retornará 30.</span><span class="sxs-lookup"><span data-stu-id="ea83f-129">Returns 30.</span></span>
  

