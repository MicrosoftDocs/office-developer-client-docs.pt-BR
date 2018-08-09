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
description: Retorna verdadeiro (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772440"
---
# <a name="or-function"></a><span data-ttu-id="f1797-103">Função OR</span><span class="sxs-lookup"><span data-stu-id="f1797-103">OR Function</span></span>

<span data-ttu-id="f1797-104">Retorna verdadeiro (1) se qualquer uma das expressões lógicas passadas como parâmetros forem TRUE.</span><span class="sxs-lookup"><span data-stu-id="f1797-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f1797-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1797-105">Syntax</span></span>

<span data-ttu-id="f1797-106">OU (* * *expressão lógica1* * *, * * *expressão lógica2* * *,..., * * *expressão lógicaN* * *)</span><span class="sxs-lookup"><span data-stu-id="f1797-106">OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f1797-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1797-107">Parameters</span></span>

|<span data-ttu-id="f1797-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1797-108">**Name**</span></span>|<span data-ttu-id="f1797-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f1797-109">**Required/Optional**</span></span>|<span data-ttu-id="f1797-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f1797-110">**Data Type**</span></span>|<span data-ttu-id="f1797-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f1797-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f1797-112">_expressão lógica1_</span><span class="sxs-lookup"><span data-stu-id="f1797-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="f1797-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f1797-113">Required</span></span>  <br/> |<span data-ttu-id="f1797-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f1797-114">**String**</span></span> <br/> |<span data-ttu-id="f1797-115">A primeira expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="f1797-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="f1797-116">_expressão lógica2_</span><span class="sxs-lookup"><span data-stu-id="f1797-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="f1797-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f1797-117">Required</span></span>  <br/> |<span data-ttu-id="f1797-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f1797-118">**String**</span></span> <br/> |<span data-ttu-id="f1797-119">A segunda expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="f1797-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="f1797-120">_expressão lógicaN_</span><span class="sxs-lookup"><span data-stu-id="f1797-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="f1797-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f1797-121">Required</span></span>  <br/> |<span data-ttu-id="f1797-122">**String**</span><span class="sxs-lookup"><span data-stu-id="f1797-122">**String**</span></span> <br/> |<span data-ttu-id="f1797-123">A enésima expressão cuja veracidade você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="f1797-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f1797-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f1797-124">Return value</span></span>

<span data-ttu-id="f1797-125">Booliano</span><span class="sxs-lookup"><span data-stu-id="f1797-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1797-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1797-126">Remarks</span></span>

<span data-ttu-id="f1797-p101">Qualquer expressão avaliada para um valor diferente de zero é considerada VERDADEIRO. Se todas as expressões lógicas forem FALSO ou iguais a 0, essa função retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="f1797-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f1797-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f1797-129">Example</span></span>

<span data-ttu-id="f1797-130">OU (altura \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="f1797-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="f1797-p102">Retornará VERDADEIRO (1) se qualquer uma das expressões for VERDADEIRO. Retornará FALSO (0) somente se ambas as expressões forem FALSO.</span><span class="sxs-lookup"><span data-stu-id="f1797-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

