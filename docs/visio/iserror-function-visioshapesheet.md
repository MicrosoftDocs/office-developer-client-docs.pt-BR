---
title: Função ISERROR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Retorna TRUE se o valor de cellreference for qualquer tipo de erro; caso contrário, retornará FALSE. A função isERROr é usada em fórmulas que se referem a outra célula.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421540"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="49b0a-104">Função ISERROR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="49b0a-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="49b0a-105">Retorna TRUE se o valor de _cellreference_ for qualquer tipo de erro; caso contrário, retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="49b0a-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="49b0a-106">A função isERROr é usada em fórmulas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="49b0a-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="49b0a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49b0a-107">Syntax</span></span>

<span data-ttu-id="49b0a-108">IsERROr (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="49b0a-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="49b0a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49b0a-109">Parameters</span></span>

|<span data-ttu-id="49b0a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="49b0a-110">**Name**</span></span>|<span data-ttu-id="49b0a-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="49b0a-111">**Required/Optional**</span></span>|<span data-ttu-id="49b0a-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="49b0a-112">**Data Type**</span></span>|<span data-ttu-id="49b0a-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="49b0a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="49b0a-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="49b0a-114">_cellreference_</span></span> <br/> |<span data-ttu-id="49b0a-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="49b0a-115">Required</span></span>  <br/> |<span data-ttu-id="49b0a-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="49b0a-116">**String**</span></span> <br/> |<span data-ttu-id="49b0a-117">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="49b0a-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="49b0a-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="49b0a-118">Example 1</span></span>

|<span data-ttu-id="49b0a-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="49b0a-119">**Cell**</span></span>|<span data-ttu-id="49b0a-120">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="49b0a-120">**Formula**</span></span>|<span data-ttu-id="49b0a-121">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="49b0a-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="49b0a-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="49b0a-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="49b0a-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="49b0a-123">=NA( )</span></span>  <br/> |<span data-ttu-id="49b0a-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="49b0a-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="49b0a-125">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="49b0a-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="49b0a-126">= IsERROr (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="49b0a-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="49b0a-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="49b0a-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="49b0a-p103">Retornará VERDADEIRO porque o erro de #N/A! é reconhecido pela função ISERROR. Utilize a função ISERR para localizar todos os tipos de erro, exceto #N/A!.</span><span class="sxs-lookup"><span data-stu-id="49b0a-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="49b0a-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="49b0a-132">Example 2</span></span>

|<span data-ttu-id="49b0a-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="49b0a-133">**Cell**</span></span>|<span data-ttu-id="49b0a-134">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="49b0a-134">**Formula**</span></span>|<span data-ttu-id="49b0a-135">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="49b0a-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="49b0a-136">Scratch. X1</span><span class="sxs-lookup"><span data-stu-id="49b0a-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="49b0a-137">= "House"</span><span class="sxs-lookup"><span data-stu-id="49b0a-137">="House"</span></span>  <br/> |<span data-ttu-id="49b0a-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="49b0a-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="49b0a-139">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="49b0a-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="49b0a-140">= IsERROr (Scratch. X1)</span><span class="sxs-lookup"><span data-stu-id="49b0a-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="49b0a-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="49b0a-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="49b0a-p104">Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERROR. Para criar uma expressão com base no erro de #VALUE!, utilize a função ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="49b0a-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

