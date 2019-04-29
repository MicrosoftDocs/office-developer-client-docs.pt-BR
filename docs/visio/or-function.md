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
description: Retorna TRUE (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433504"
---
# <a name="or-function"></a><span data-ttu-id="2781a-103">Função OR</span><span class="sxs-lookup"><span data-stu-id="2781a-103">OR Function</span></span>

<span data-ttu-id="2781a-104">Retorna TRUE (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.</span><span class="sxs-lookup"><span data-stu-id="2781a-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2781a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2781a-105">Syntax</span></span>

<span data-ttu-id="2781a-106">ou (\* \* *logicalexpression1* \* \*, \* \* *logicalexpression2* \* \*,..., \* \* *logicalexpressionN* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2781a-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2781a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2781a-107">Parameters</span></span>

|<span data-ttu-id="2781a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2781a-108">**Name**</span></span>|<span data-ttu-id="2781a-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2781a-109">**Required/Optional**</span></span>|<span data-ttu-id="2781a-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2781a-110">**Data Type**</span></span>|<span data-ttu-id="2781a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2781a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2781a-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="2781a-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="2781a-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2781a-113">Required</span></span>  <br/> |<span data-ttu-id="2781a-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2781a-114">**String**</span></span> <br/> |<span data-ttu-id="2781a-115">A primeira expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="2781a-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2781a-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="2781a-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="2781a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2781a-117">Required</span></span>  <br/> |<span data-ttu-id="2781a-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2781a-118">**String**</span></span> <br/> |<span data-ttu-id="2781a-119">A segunda expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="2781a-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2781a-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="2781a-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="2781a-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2781a-121">Required</span></span>  <br/> |<span data-ttu-id="2781a-122">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2781a-122">**String**</span></span> <br/> |<span data-ttu-id="2781a-123">A enésima expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="2781a-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2781a-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2781a-124">Return value</span></span>

<span data-ttu-id="2781a-125">Booliano</span><span class="sxs-lookup"><span data-stu-id="2781a-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2781a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="2781a-126">Remarks</span></span>

<span data-ttu-id="2781a-p101">Qualquer expressão avaliada para um valor diferente de zero é considerada VERDADEIRO. Se todas as expressões lógicas forem FALSO ou iguais a 0, essa função retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="2781a-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2781a-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2781a-129">Example</span></span>

<span data-ttu-id="2781a-130">OU (altura \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="2781a-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="2781a-131">Retornará VERDADEIRO (1) se qualquer uma das expressões for VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="2781a-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="2781a-132">Retornará FALSO (0) somente se ambas as expressões forem FALSO.</span><span class="sxs-lookup"><span data-stu-id="2781a-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

