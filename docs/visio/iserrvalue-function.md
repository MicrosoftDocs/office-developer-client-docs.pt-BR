---
title: Função ISERRVALUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Retorna TRUE se o valor de cellreference for o tipo de erro #VALUE, onde um argumento na fórmula é do tipo errado. A função ISERRVALUE é usada em expressões lógicas que se referem a outra célula.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404425"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="78488-104">Função ISERRVALUE</span><span class="sxs-lookup"><span data-stu-id="78488-104">ISERRVALUE Function</span></span>

<span data-ttu-id="78488-105">Retorna TRUE se o valor de _cellreference_ for o tipo de erro #VALUE, onde um argumento na fórmula é do tipo errado.</span><span class="sxs-lookup"><span data-stu-id="78488-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="78488-106">A função ISERRVALUE é usada em expressões lógicas que se referem a outra célula.</span><span class="sxs-lookup"><span data-stu-id="78488-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78488-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78488-107">Syntax</span></span>

<span data-ttu-id="78488-108">ISERRVALUE (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="78488-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78488-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78488-109">Parameters</span></span>

|<span data-ttu-id="78488-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="78488-110">**Name**</span></span>|<span data-ttu-id="78488-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="78488-111">**Required/Optional**</span></span>|<span data-ttu-id="78488-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="78488-112">**Data Type**</span></span>|<span data-ttu-id="78488-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="78488-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78488-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="78488-114">_cellreference_</span></span> <br/> |<span data-ttu-id="78488-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="78488-115">Required</span></span>  <br/> |<span data-ttu-id="78488-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78488-116">**String**</span></span> <br/> |<span data-ttu-id="78488-117">Referência a uma célula.</span><span class="sxs-lookup"><span data-stu-id="78488-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78488-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="78488-118">Remarks</span></span>

<span data-ttu-id="78488-p103">As células transitórias de A a D não retornarão um erro de #VALUE! porque a fórmula pode conter números e letras na mesma sequência de caracteres. As células X e Y devem conter apenas números.</span><span class="sxs-lookup"><span data-stu-id="78488-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="78488-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78488-122">Example 1</span></span>

|<span data-ttu-id="78488-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="78488-123">**Cell**</span></span>|<span data-ttu-id="78488-124">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="78488-124">**Formula**</span></span>|<span data-ttu-id="78488-125">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="78488-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78488-126">Scratch. X1</span><span class="sxs-lookup"><span data-stu-id="78488-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="78488-127">="Casa"</span><span class="sxs-lookup"><span data-stu-id="78488-127">= "House"</span></span>  <br/> |<span data-ttu-id="78488-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="78488-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="78488-129">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="78488-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="78488-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="78488-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="78488-131">duas</span><span class="sxs-lookup"><span data-stu-id="78488-131">2</span></span>  <br/> |
   
<span data-ttu-id="78488-p104">Retornará 2 porque o valor retornado é um erro de #VALUE! e a expressão instrui o Microsoft Visio a retornar um 2 no lugar do erro.</span><span class="sxs-lookup"><span data-stu-id="78488-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="78488-134">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="78488-134">Example 2</span></span>

|<span data-ttu-id="78488-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="78488-135">**Cell**</span></span>|<span data-ttu-id="78488-136">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="78488-136">**Formula**</span></span>|<span data-ttu-id="78488-137">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="78488-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78488-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="78488-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="78488-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="78488-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="78488-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="78488-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="78488-141">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="78488-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="78488-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="78488-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="78488-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="78488-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="78488-p105">Retornará 12 porque o valor retornado não é um erro de #VALUE! e a expressão instrui o Visio a retornar o valor da célula original.</span><span class="sxs-lookup"><span data-stu-id="78488-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

