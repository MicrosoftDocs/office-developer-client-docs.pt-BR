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
description: Retorna o ângulo entre o vetor representado por x, y e a direção da x-eixo. O resultado é um número na unidade atual de medida para ângulos.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771264"
---
# <a name="atan2-function"></a><span data-ttu-id="00145-104">Função ATAN2</span><span class="sxs-lookup"><span data-stu-id="00145-104">ATAN2 Function</span></span>

<span data-ttu-id="00145-105">Retorna o ângulo entre o vetor representado por *x, y* e a direção da *x* -eixo.</span><span class="sxs-lookup"><span data-stu-id="00145-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="00145-106">O resultado é um número na unidade atual de medida para ângulos.</span><span class="sxs-lookup"><span data-stu-id="00145-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00145-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00145-107">Syntax</span></span>

<span data-ttu-id="00145-108">ATAN2 (* * *y* * *, * * *x* * *)</span><span class="sxs-lookup"><span data-stu-id="00145-108">ATAN2(** *y* **, ** *x* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00145-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00145-109">Parameters</span></span>

|<span data-ttu-id="00145-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="00145-110">**Name**</span></span>|<span data-ttu-id="00145-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="00145-111">**Required/Optional**</span></span>|<span data-ttu-id="00145-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="00145-112">**Data Type**</span></span>|<span data-ttu-id="00145-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="00145-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00145-114">_y_</span><span class="sxs-lookup"><span data-stu-id="00145-114">_y_</span></span> <br/> |<span data-ttu-id="00145-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="00145-115">Required</span></span>  <br/> |<span data-ttu-id="00145-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="00145-116">**Numeric**</span></span> <br/> |<span data-ttu-id="00145-117">_Y_-valor do ponto.</span><span class="sxs-lookup"><span data-stu-id="00145-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="00145-118">_x_</span><span class="sxs-lookup"><span data-stu-id="00145-118">_x_</span></span> <br/> |<span data-ttu-id="00145-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="00145-119">Required</span></span>  <br/> |<span data-ttu-id="00145-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="00145-120">**Numeric**</span></span> <br/> |<span data-ttu-id="00145-121">_X_-o valor do ponto.</span><span class="sxs-lookup"><span data-stu-id="00145-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00145-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="00145-122">Remarks</span></span>

<span data-ttu-id="00145-123">O arco tangente é o ângulo medido no sentido anti-horário do positivo *x* -eixo para uma linha que intercepta a origem (0,0) e o ponto representado por *x* e *y* .</span><span class="sxs-lookup"><span data-stu-id="00145-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="00145-124">No Microsoft Visio, ATAN2(0,0) retornará 0.</span><span class="sxs-lookup"><span data-stu-id="00145-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="00145-125">Para forçar o resultado de ATAN2 para uma medida angular diferente, use as funções DEG ou RAD.</span><span class="sxs-lookup"><span data-stu-id="00145-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="00145-126">A função ATAN2 é a antifunção da função TAN.</span><span class="sxs-lookup"><span data-stu-id="00145-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="00145-127">A função ATAN2 retorna o ângulo cujo ângulo é igual a *y* dividido por *x* .</span><span class="sxs-lookup"><span data-stu-id="00145-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="00145-128">Se ATAN2 (*y, x*) representando um ângulo no triângulo, *y* é o "lado oposto" e *x* é o "lado adjacente", portanto, a função poderia ser gravada como ATAN2.</span><span class="sxs-lookup"><span data-stu-id="00145-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="00145-129">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00145-129">Example 1</span></span>

<span data-ttu-id="00145-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="00145-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="00145-131">Retorna 29,0456 graus.</span><span class="sxs-lookup"><span data-stu-id="00145-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="00145-132">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00145-132">Example 2</span></span>

<span data-ttu-id="00145-133">ATAN2(1,SQRT(3))</span><span class="sxs-lookup"><span data-stu-id="00145-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="00145-134">Retorna 30 graus.</span><span class="sxs-lookup"><span data-stu-id="00145-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="00145-135">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="00145-135">Example 3</span></span>

<span data-ttu-id="00145-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="00145-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="00145-137">Retorna 45 graus.</span><span class="sxs-lookup"><span data-stu-id="00145-137">Returns 45 deg</span></span>
  

