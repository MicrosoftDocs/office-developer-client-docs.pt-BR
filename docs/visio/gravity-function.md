---
title: Função GRAVITY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcula a ângulo correto do bloco de texto de rotação para a rotação da forma indicado impedir que o texto desativando cabeça para baixo.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19771979"
---
# <a name="gravity-function"></a><span data-ttu-id="5f462-103">Função GRAVITY</span><span class="sxs-lookup"><span data-stu-id="5f462-103">GRAVITY Function</span></span>

<span data-ttu-id="5f462-104">Calcula a ângulo correto do bloco de texto de rotação para a rotação da forma indicado impedir que o texto desativando cabeça para baixo.</span><span class="sxs-lookup"><span data-stu-id="5f462-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5f462-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f462-105">Syntax</span></span>

<span data-ttu-id="5f462-106">GRAVITY (* * *ângulo* * *, [* * *limit1* * *], [* * *limit2* * *])</span><span class="sxs-lookup"><span data-stu-id="5f462-106">GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f462-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f462-107">Parameters</span></span>

|<span data-ttu-id="5f462-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5f462-108">**Name**</span></span>|<span data-ttu-id="5f462-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5f462-109">**Required/Optional**</span></span>|<span data-ttu-id="5f462-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5f462-110">**Data Type**</span></span>|<span data-ttu-id="5f462-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5f462-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f462-112">_ângulo_</span><span class="sxs-lookup"><span data-stu-id="5f462-112">_angle_</span></span> <br/> |<span data-ttu-id="5f462-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5f462-113">Required</span></span>  <br/> |<span data-ttu-id="5f462-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5f462-114">**String**</span></span> <br/> | <span data-ttu-id="5f462-115">O ângulo da forma.</span><span class="sxs-lookup"><span data-stu-id="5f462-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="5f462-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="5f462-116">_limit1_</span></span> <br/> |<span data-ttu-id="5f462-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="5f462-117">Optional</span></span>  <br/> |<span data-ttu-id="5f462-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5f462-118">**String**</span></span> <br/> |<span data-ttu-id="5f462-p101">O padrão é de 90 graus.</span><span class="sxs-lookup"><span data-stu-id="5f462-p101">First limit of rotation. Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="5f462-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="5f462-121">_limit2_</span></span> <br/> |<span data-ttu-id="5f462-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="5f462-122">Optional</span></span>  <br/> |<span data-ttu-id="5f462-123">**String**</span><span class="sxs-lookup"><span data-stu-id="5f462-123">**String**</span></span> <br/> |<span data-ttu-id="5f462-p102">Segundo limite de rotação. O padrão é de 270 graus.</span><span class="sxs-lookup"><span data-stu-id="5f462-p102">Second limit of rotation. Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5f462-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5f462-126">Return value</span></span>

<span data-ttu-id="5f462-127">String</span><span class="sxs-lookup"><span data-stu-id="5f462-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f462-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f462-128">Remarks</span></span>

<span data-ttu-id="5f462-129">A função GRAVITY é normalmente usada na célula TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="5f462-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="5f462-130">O valor retornado será de 180 graus se o _angle_ estiver entre os valores especificados por _limit1_ e _limit2_; Caso contrário, o valor retornado será 0 grau.</span><span class="sxs-lookup"><span data-stu-id="5f462-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="5f462-p103">Todos os argumentos são automaticamente normalizados entre 0 e 360 graus pela função. Se um argumento não especificar unidades, são adotados radianos.</span><span class="sxs-lookup"><span data-stu-id="5f462-p103">All of the arguments are automatically normalized between 0 and 360 degrees by the function. If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5f462-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f462-133">Example 1</span></span>

<span data-ttu-id="5f462-134">GRAVITY(Ângulo)</span><span class="sxs-lookup"><span data-stu-id="5f462-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="5f462-135">Retorna 180 graus se o *angle* estiver entre 90 e 270 graus; Caso contrário, retornará 0 grau.</span><span class="sxs-lookup"><span data-stu-id="5f462-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="5f462-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5f462-136">Example 2</span></span>

<span data-ttu-id="5f462-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="5f462-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="5f462-138">Retorna 180 graus, porque 2 radianos fica entre 90 e 270 graus.</span><span class="sxs-lookup"><span data-stu-id="5f462-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5f462-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5f462-139">Example 3</span></span>

<span data-ttu-id="5f462-140">GRAVITY(100 graus, 110 graus, 290 graus)</span><span class="sxs-lookup"><span data-stu-id="5f462-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="5f462-141">Retorna 0 grau.</span><span class="sxs-lookup"><span data-stu-id="5f462-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="5f462-142">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="5f462-142">Example 4</span></span>

<span data-ttu-id="5f462-143">GRAVITY(100 graus, 290 graus, 110 graus)</span><span class="sxs-lookup"><span data-stu-id="5f462-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="5f462-144">Retorna 0 grau.</span><span class="sxs-lookup"><span data-stu-id="5f462-144">Returns 0 degrees.</span></span>
  

