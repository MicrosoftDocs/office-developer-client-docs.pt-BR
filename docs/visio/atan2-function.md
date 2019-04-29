---
title: Função ATAN2
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Retorna o ângulo entre o vetor representado por x, y e a direção do eixo x. O resultado é um número na unidade de medida atual para ângulos.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436479"
---
# <a name="atan2-function"></a><span data-ttu-id="06aeb-104">Função ATAN2</span><span class="sxs-lookup"><span data-stu-id="06aeb-104">ATAN2 Function</span></span>

<span data-ttu-id="06aeb-105">Retorna o ângulo entre o vetor representado por *x, y* e a direção do eixo *x* .</span><span class="sxs-lookup"><span data-stu-id="06aeb-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="06aeb-106">O resultado é um número na unidade de medida atual para ângulos.</span><span class="sxs-lookup"><span data-stu-id="06aeb-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="06aeb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06aeb-107">Syntax</span></span>

<span data-ttu-id="06aeb-108">ATAN2 (\* \* *y* \* \*, \* \* *x* \* \*)</span><span class="sxs-lookup"><span data-stu-id="06aeb-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="06aeb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06aeb-109">Parameters</span></span>

|<span data-ttu-id="06aeb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="06aeb-110">**Name**</span></span>|<span data-ttu-id="06aeb-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="06aeb-111">**Required/Optional**</span></span>|<span data-ttu-id="06aeb-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="06aeb-112">**Data Type**</span></span>|<span data-ttu-id="06aeb-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="06aeb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="06aeb-114">_y_</span><span class="sxs-lookup"><span data-stu-id="06aeb-114">_y_</span></span> <br/> |<span data-ttu-id="06aeb-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="06aeb-115">Required</span></span>  <br/> |<span data-ttu-id="06aeb-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="06aeb-116">**Numeric**</span></span> <br/> |<span data-ttu-id="06aeb-117">O valor _y_do ponto.</span><span class="sxs-lookup"><span data-stu-id="06aeb-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="06aeb-118">_x_</span><span class="sxs-lookup"><span data-stu-id="06aeb-118">_x_</span></span> <br/> |<span data-ttu-id="06aeb-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="06aeb-119">Required</span></span>  <br/> |<span data-ttu-id="06aeb-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="06aeb-120">**Numeric**</span></span> <br/> |<span data-ttu-id="06aeb-121">O valor _x_do ponto.</span><span class="sxs-lookup"><span data-stu-id="06aeb-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06aeb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="06aeb-122">Remarks</span></span>

<span data-ttu-id="06aeb-123">O arco tangente é medido no sentido anti-horário do eixo *x* positivo para uma linha que cruza a origem (0, 0) e o ponto representado por *x* e *y* .</span><span class="sxs-lookup"><span data-stu-id="06aeb-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="06aeb-124">No Microsoft Visio, ATAN2(0,0) retornará 0.</span><span class="sxs-lookup"><span data-stu-id="06aeb-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="06aeb-125">Para forçar o resultado de ATAN2 para uma medida angular diferente, utilize as funções DEG ou RAD.</span><span class="sxs-lookup"><span data-stu-id="06aeb-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="06aeb-126">A função ATAN2 é a antifunção da função TAN.</span><span class="sxs-lookup"><span data-stu-id="06aeb-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="06aeb-127">A função ATAN2 retorna o ângulo cujo ângulo é igual a *y* dividido por *x* .</span><span class="sxs-lookup"><span data-stu-id="06aeb-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="06aeb-128">Se ATAN2 (*y, x*) representar um ângulo em um triângulo à direita, *y* será o "lado oposto" e *x* será o "lado adjacente", para que a função possa ser gravada como ATAN2 (oposto, adjacente).</span><span class="sxs-lookup"><span data-stu-id="06aeb-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="06aeb-129">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06aeb-129">Example 1</span></span>

<span data-ttu-id="06aeb-130">ATAN2 (1,25, 2,25)</span><span class="sxs-lookup"><span data-stu-id="06aeb-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="06aeb-131">Retorna 29,0456 graus.</span><span class="sxs-lookup"><span data-stu-id="06aeb-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="06aeb-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06aeb-132">Example 2</span></span>

<span data-ttu-id="06aeb-133">ATAN2 (1, SQRT (3))</span><span class="sxs-lookup"><span data-stu-id="06aeb-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="06aeb-134">Retorna 30 graus.</span><span class="sxs-lookup"><span data-stu-id="06aeb-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="06aeb-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="06aeb-135">Example 3</span></span>

<span data-ttu-id="06aeb-136">ATAN2 (1, 1)</span><span class="sxs-lookup"><span data-stu-id="06aeb-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="06aeb-137">Retorna 45 graus.</span><span class="sxs-lookup"><span data-stu-id="06aeb-137">Returns 45 deg</span></span>
  

