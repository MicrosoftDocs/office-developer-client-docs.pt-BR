---
title: Função ISERR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Retorna TRUE se o valor de cellreference for qualquer tipo de erro, exceto #N/A; caso contrário, retornará FALSE. A função ÉERRO é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432104"
---
# <a name="iserr-function"></a><span data-ttu-id="53329-104">Função ISERR</span><span class="sxs-lookup"><span data-stu-id="53329-104">ISERR Function</span></span>

<span data-ttu-id="53329-105">Retorna TRUE se o valor de _cellreference_ for qualquer tipo de erro, exceto #N/a; caso contrário, retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="53329-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="53329-106">A função ÉERRO é usada em fórmulas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="53329-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53329-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53329-107">Syntax</span></span>

<span data-ttu-id="53329-108">ÉERRO (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="53329-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="53329-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53329-109">Parameters</span></span>

|<span data-ttu-id="53329-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="53329-110">**Name**</span></span>|<span data-ttu-id="53329-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="53329-111">**Required/Optional**</span></span>|<span data-ttu-id="53329-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="53329-112">**Data Type**</span></span>|<span data-ttu-id="53329-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="53329-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="53329-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="53329-114">_cellreference_</span></span> <br/> |<span data-ttu-id="53329-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="53329-115">Required</span></span>  <br/> |<span data-ttu-id="53329-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53329-116">**String**</span></span> <br/> |<span data-ttu-id="53329-117">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="53329-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="53329-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53329-118">Example 1</span></span>

|<span data-ttu-id="53329-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="53329-119">**Cell**</span></span>|<span data-ttu-id="53329-120">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="53329-120">**Formula**</span></span>|<span data-ttu-id="53329-121">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="53329-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53329-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="53329-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="53329-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="53329-123">=NA( )</span></span>  <br/> |<span data-ttu-id="53329-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="53329-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="53329-125">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="53329-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="53329-126">= ÉERRO (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="53329-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="53329-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="53329-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="53329-p103">Retornará FALSO porque o erro de #N/A! não é reconhecido pela função ISERR. Utilize a função ISERROR para localizar todos os tipos de erros.</span><span class="sxs-lookup"><span data-stu-id="53329-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="53329-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53329-131">Example 2</span></span>

|<span data-ttu-id="53329-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="53329-132">**Cell**</span></span>|<span data-ttu-id="53329-133">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="53329-133">**Formula**</span></span>|<span data-ttu-id="53329-134">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="53329-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53329-135">Scratch. X1</span><span class="sxs-lookup"><span data-stu-id="53329-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="53329-136">= "House"</span><span class="sxs-lookup"><span data-stu-id="53329-136">="House"</span></span>  <br/> |<span data-ttu-id="53329-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="53329-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="53329-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="53329-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="53329-139">= ÉERRO (Scratch. X1)</span><span class="sxs-lookup"><span data-stu-id="53329-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="53329-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="53329-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="53329-p104">Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERR.</span><span class="sxs-lookup"><span data-stu-id="53329-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

