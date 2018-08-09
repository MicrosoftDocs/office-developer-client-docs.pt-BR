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
description: Retorna TRUE se o valor de referênciadecélula for qualquer tipo de erro; Caso contrário, ele retornará FALSE. A função ISERROR é usada em fórmulas que se referem a outra célula.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772112"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="321e7-104">Função ISERROR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="321e7-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="321e7-105">Retorna TRUE se o valor de _referênciadecélula_ for qualquer tipo de erro; Caso contrário, ele retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="321e7-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="321e7-106">A função ISERROR é usada em fórmulas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="321e7-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="321e7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="321e7-107">Syntax</span></span>

<span data-ttu-id="321e7-108">ISERROR (* * *referênciadecélula* * *)</span><span class="sxs-lookup"><span data-stu-id="321e7-108">ISERROR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="321e7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="321e7-109">Parameters</span></span>

|<span data-ttu-id="321e7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="321e7-110">**Name**</span></span>|<span data-ttu-id="321e7-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="321e7-111">**Required/Optional**</span></span>|<span data-ttu-id="321e7-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="321e7-112">**Data Type**</span></span>|<span data-ttu-id="321e7-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="321e7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="321e7-114">_referênciadecélula_</span><span class="sxs-lookup"><span data-stu-id="321e7-114">_cellreference_</span></span> <br/> |<span data-ttu-id="321e7-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="321e7-115">Required</span></span>  <br/> |<span data-ttu-id="321e7-116">**String**</span><span class="sxs-lookup"><span data-stu-id="321e7-116">**String**</span></span> <br/> |<span data-ttu-id="321e7-117">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="321e7-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="321e7-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="321e7-118">Example 1</span></span>

|<span data-ttu-id="321e7-119">**Célula**</span><span class="sxs-lookup"><span data-stu-id="321e7-119">**Cell**</span></span>|<span data-ttu-id="321e7-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="321e7-120">**Formula**</span></span>|<span data-ttu-id="321e7-121">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="321e7-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="321e7-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="321e7-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="321e7-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="321e7-123">=NA( )</span></span>  <br/> |<span data-ttu-id="321e7-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="321e7-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="321e7-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="321e7-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="321e7-126">=IsError(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="321e7-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="321e7-127">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="321e7-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="321e7-p103">Retornará VERDADEIRO porque o erro de #N/A! é reconhecido pela função ISERROR. Utilize a função ISERR para localizar todos os tipos de erro, exceto #N/A!.</span><span class="sxs-lookup"><span data-stu-id="321e7-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="321e7-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="321e7-132">Example 2</span></span>

|<span data-ttu-id="321e7-133">**Célula**</span><span class="sxs-lookup"><span data-stu-id="321e7-133">**Cell**</span></span>|<span data-ttu-id="321e7-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="321e7-134">**Formula**</span></span>|<span data-ttu-id="321e7-135">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="321e7-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="321e7-136">Y1</span><span class="sxs-lookup"><span data-stu-id="321e7-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="321e7-137">="Casa"</span><span class="sxs-lookup"><span data-stu-id="321e7-137">="House"</span></span>  <br/> |<span data-ttu-id="321e7-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="321e7-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="321e7-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="321e7-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="321e7-140">=IsError(Scratch.x1)</span><span class="sxs-lookup"><span data-stu-id="321e7-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="321e7-141">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="321e7-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="321e7-p104">Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERROR. Para criar uma expressão com base no erro de #VALUE!, utilize a função ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="321e7-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

