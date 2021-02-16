---
title: Função OR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Retorna VERDADEIRO (1) se qualquer uma das expressões lógicas passadas como parâmetros for VERDADEIRO.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433504"
---
# <a name="or-function"></a><span data-ttu-id="21d55-103">Função OR</span><span class="sxs-lookup"><span data-stu-id="21d55-103">OR Function</span></span>

<span data-ttu-id="21d55-104">Retorna VERDADEIRO (1) se qualquer uma das expressões lógicas passadas como parâmetros for VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="21d55-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="21d55-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21d55-105">Syntax</span></span>

<span data-ttu-id="21d55-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="21d55-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21d55-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21d55-107">Parameters</span></span>

|<span data-ttu-id="21d55-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="21d55-108">**Name**</span></span>|<span data-ttu-id="21d55-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="21d55-109">**Required/Optional**</span></span>|<span data-ttu-id="21d55-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="21d55-110">**Data Type**</span></span>|<span data-ttu-id="21d55-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="21d55-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21d55-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="21d55-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="21d55-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="21d55-113">Required</span></span>  <br/> |<span data-ttu-id="21d55-114">**String**</span><span class="sxs-lookup"><span data-stu-id="21d55-114">**String**</span></span> <br/> |<span data-ttu-id="21d55-115">A primeira expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="21d55-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="21d55-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="21d55-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="21d55-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="21d55-117">Required</span></span>  <br/> |<span data-ttu-id="21d55-118">**String**</span><span class="sxs-lookup"><span data-stu-id="21d55-118">**String**</span></span> <br/> |<span data-ttu-id="21d55-119">A segunda expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="21d55-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="21d55-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="21d55-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="21d55-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="21d55-121">Required</span></span>  <br/> |<span data-ttu-id="21d55-122">**String**</span><span class="sxs-lookup"><span data-stu-id="21d55-122">**String**</span></span> <br/> |<span data-ttu-id="21d55-123">A enésima expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="21d55-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="21d55-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="21d55-124">Return value</span></span>

<span data-ttu-id="21d55-125">Booliano</span><span class="sxs-lookup"><span data-stu-id="21d55-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21d55-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="21d55-126">Remarks</span></span>

<span data-ttu-id="21d55-p101">Qualquer expressão avaliada para um valor diferente de zero é considerada VERDADEIRO. Se todas as expressões lógicas forem FALSO ou iguais a 0, essa função retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="21d55-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="21d55-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="21d55-129">Example</span></span>

<span data-ttu-id="21d55-130">OR(Height \> 1,PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="21d55-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="21d55-131">Retornará VERDADEIRO (1) se qualquer uma das expressões for VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="21d55-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="21d55-132">Retornará FALSO (0) somente se ambas as expressões forem FALSO.</span><span class="sxs-lookup"><span data-stu-id="21d55-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

