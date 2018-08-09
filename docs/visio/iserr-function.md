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
description: 'Retorna VERDADEIRO se o valor de referênciadecélula for qualquer tipo de erro exceto # n/d; Caso contrário, ele retornará FALSE. A função ISERR é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772098"
---
# <a name="iserr-function"></a><span data-ttu-id="f002f-104">Função ISERR</span><span class="sxs-lookup"><span data-stu-id="f002f-104">ISERR Function</span></span>

<span data-ttu-id="f002f-105">Retorna TRUE se o valor de _referênciadecélula_ for qualquer tipo de erro exceto # n/d; Caso contrário, ele retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="f002f-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="f002f-106">A função ISERR é usada em fórmulas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="f002f-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f002f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f002f-107">Syntax</span></span>

<span data-ttu-id="f002f-108">ÉERRO (* * *referênciadecélula* * *)</span><span class="sxs-lookup"><span data-stu-id="f002f-108">ISERR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f002f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f002f-109">Parameters</span></span>

|<span data-ttu-id="f002f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="f002f-110">**Name**</span></span>|<span data-ttu-id="f002f-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f002f-111">**Required/Optional**</span></span>|<span data-ttu-id="f002f-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f002f-112">**Data Type**</span></span>|<span data-ttu-id="f002f-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f002f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f002f-114">_referênciadecélula_</span><span class="sxs-lookup"><span data-stu-id="f002f-114">_cellreference_</span></span> <br/> |<span data-ttu-id="f002f-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f002f-115">Required</span></span>  <br/> |<span data-ttu-id="f002f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="f002f-116">**String**</span></span> <br/> |<span data-ttu-id="f002f-117">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="f002f-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="f002f-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f002f-118">Example 1</span></span>

|<span data-ttu-id="f002f-119">**Célula**</span><span class="sxs-lookup"><span data-stu-id="f002f-119">**Cell**</span></span>|<span data-ttu-id="f002f-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="f002f-120">**Formula**</span></span>|<span data-ttu-id="f002f-121">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="f002f-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f002f-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="f002f-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="f002f-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="f002f-123">=NA( )</span></span>  <br/> |<span data-ttu-id="f002f-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="f002f-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="f002f-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="f002f-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="f002f-126">=ISERR(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="f002f-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="f002f-127">FALSO</span><span class="sxs-lookup"><span data-stu-id="f002f-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="f002f-p103">Retornará FALSO porque o erro de #N/A! não é reconhecido pela função ISERR. Utilize a função ISERROR para localizar todos os tipos de erros.</span><span class="sxs-lookup"><span data-stu-id="f002f-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f002f-131">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f002f-131">Example 2</span></span>

|<span data-ttu-id="f002f-132">**Célula**</span><span class="sxs-lookup"><span data-stu-id="f002f-132">**Cell**</span></span>|<span data-ttu-id="f002f-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="f002f-133">**Formula**</span></span>|<span data-ttu-id="f002f-134">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="f002f-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f002f-135">Y1</span><span class="sxs-lookup"><span data-stu-id="f002f-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="f002f-136">="Casa"</span><span class="sxs-lookup"><span data-stu-id="f002f-136">="House"</span></span>  <br/> |<span data-ttu-id="f002f-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="f002f-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="f002f-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="f002f-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="f002f-139">=ISERR(Scratch.x1)</span><span class="sxs-lookup"><span data-stu-id="f002f-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="f002f-140">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="f002f-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="f002f-p104">Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERR.</span><span class="sxs-lookup"><span data-stu-id="f002f-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

