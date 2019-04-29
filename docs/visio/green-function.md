---
title: Função GREEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Retorna o componente verde de uma cor.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438103"
---
# <a name="green-function"></a><span data-ttu-id="0a481-103">Função GREEN</span><span class="sxs-lookup"><span data-stu-id="0a481-103">GREEN Function</span></span>

<span data-ttu-id="0a481-104">Retorna o componente verde de uma cor.</span><span class="sxs-lookup"><span data-stu-id="0a481-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0a481-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a481-105">Syntax</span></span>

<span data-ttu-id="0a481-106">VERDE (\* \* *expressão* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0a481-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a481-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a481-107">Parameters</span></span>

|<span data-ttu-id="0a481-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a481-108">**Name**</span></span>|<span data-ttu-id="0a481-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="0a481-109">**Required/Optional**</span></span>|<span data-ttu-id="0a481-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="0a481-110">**Data Type**</span></span>|<span data-ttu-id="0a481-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0a481-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a481-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="0a481-112">_expression_</span></span> <br/> |<span data-ttu-id="0a481-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a481-113">Required</span></span>  <br/> |<span data-ttu-id="0a481-114">**Vai**</span><span class="sxs-lookup"><span data-stu-id="0a481-114">**Varies**</span></span> <br/> |<span data-ttu-id="0a481-115">Um índice de uma cor na tabela de cores do documento, uma expressão que resolve para uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cor.</span><span class="sxs-lookup"><span data-stu-id="0a481-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0a481-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0a481-116">Return value</span></span>

<span data-ttu-id="0a481-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="0a481-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a481-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a481-118">Remarks</span></span>

<span data-ttu-id="0a481-119">O valor retornado é um número entre 0 e 255, inclusive, ou uma referência de célula que resulta em um índice.</span><span class="sxs-lookup"><span data-stu-id="0a481-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="0a481-120">Se a *expressão* for inválida, retornará 0 (preto).</span><span class="sxs-lookup"><span data-stu-id="0a481-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0a481-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a481-121">Example 1</span></span>

<span data-ttu-id="0a481-122">VERDE (planilha. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="0a481-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="0a481-123">Retornará o componente verde da cor de primeiro plano do preenchimento de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="0a481-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0a481-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0a481-124">Example 2</span></span>

<span data-ttu-id="0a481-125">VERDE (11)</span><span class="sxs-lookup"><span data-stu-id="0a481-125">GREEN(11)</span></span>
  
<span data-ttu-id="0a481-126">Retornará 128 se o documento utilizar a paleta de cores padrão do Visio, sendo amarelo escuro a cor do índice 11.</span><span class="sxs-lookup"><span data-stu-id="0a481-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0a481-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0a481-127">Example 3</span></span>

<span data-ttu-id="0a481-128">GREEN(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="0a481-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="0a481-129">Retornará 20.</span><span class="sxs-lookup"><span data-stu-id="0a481-129">Returns 20.</span></span>
  

