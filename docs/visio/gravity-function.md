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
description: Calcula o ângulo de rotação correto de um bloco de texto para a rotação de formas indicada para evitar que o texto seja virado de cabeça para baixo.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429282"
---
# <a name="gravity-function"></a><span data-ttu-id="62d52-103">Função GRAVITY</span><span class="sxs-lookup"><span data-stu-id="62d52-103">GRAVITY Function</span></span>

<span data-ttu-id="62d52-104">Calcula o ângulo de rotação correto de um bloco de texto para a rotação de formas indicada para evitar que o texto seja virado de cabeça para baixo.</span><span class="sxs-lookup"><span data-stu-id="62d52-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="62d52-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62d52-105">Syntax</span></span>

<span data-ttu-id="62d52-106">Gravidade (\* \* *Angle* \* *, [* \* *limites1* \* *], [* \* *limit2* \* \*])</span><span class="sxs-lookup"><span data-stu-id="62d52-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="62d52-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62d52-107">Parameters</span></span>

|<span data-ttu-id="62d52-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="62d52-108">**Name**</span></span>|<span data-ttu-id="62d52-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="62d52-109">**Required/Optional**</span></span>|<span data-ttu-id="62d52-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="62d52-110">**Data Type**</span></span>|<span data-ttu-id="62d52-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62d52-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="62d52-112">_ângulo_</span><span class="sxs-lookup"><span data-stu-id="62d52-112">_angle_</span></span> <br/> |<span data-ttu-id="62d52-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="62d52-113">Required</span></span>  <br/> |<span data-ttu-id="62d52-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62d52-114">**String**</span></span> <br/> | <span data-ttu-id="62d52-115">O ângulo da forma.</span><span class="sxs-lookup"><span data-stu-id="62d52-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="62d52-116">_limites1_</span><span class="sxs-lookup"><span data-stu-id="62d52-116">_limit1_</span></span> <br/> |<span data-ttu-id="62d52-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="62d52-117">Optional</span></span>  <br/> |<span data-ttu-id="62d52-118">**String**</span><span class="sxs-lookup"><span data-stu-id="62d52-118">**String**</span></span> <br/> |<span data-ttu-id="62d52-119">Primeiro limite de rotação.</span><span class="sxs-lookup"><span data-stu-id="62d52-119">First limit of rotation.</span></span> <span data-ttu-id="62d52-120">O padrão é 90 graus.</span><span class="sxs-lookup"><span data-stu-id="62d52-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="62d52-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="62d52-121">_limit2_</span></span> <br/> |<span data-ttu-id="62d52-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="62d52-122">Optional</span></span>  <br/> |<span data-ttu-id="62d52-123">**String**</span><span class="sxs-lookup"><span data-stu-id="62d52-123">**String**</span></span> <br/> |<span data-ttu-id="62d52-124">Segundo limite de rotação.</span><span class="sxs-lookup"><span data-stu-id="62d52-124">Second limit of rotation.</span></span> <span data-ttu-id="62d52-125">O padrão é de 270 graus.</span><span class="sxs-lookup"><span data-stu-id="62d52-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="62d52-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="62d52-126">Return value</span></span>

<span data-ttu-id="62d52-127">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="62d52-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62d52-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="62d52-128">Remarks</span></span>

<span data-ttu-id="62d52-129">A função GRAVITY é normalmente usada na célula TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="62d52-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="62d52-130">O valor retornado será 180 graus se _Angle_ estiver entre os valores especificados por _limites1_ e _limit2_; caso contrário, o valor retornado será 0 grau.</span><span class="sxs-lookup"><span data-stu-id="62d52-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="62d52-131">Todos os argumentos são automaticamente normalizados entre 0 e 360 graus pela função.</span><span class="sxs-lookup"><span data-stu-id="62d52-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="62d52-132">Se um argumento não especificar unidades, são adotados radianos.</span><span class="sxs-lookup"><span data-stu-id="62d52-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="62d52-133">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62d52-133">Example 1</span></span>

<span data-ttu-id="62d52-134">GRAVIDADE (angular)</span><span class="sxs-lookup"><span data-stu-id="62d52-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="62d52-135">Retorna 180 graus se o *ângulo* estiver entre 90 e 270 graus; caso contrário, retornará 0 graus.</span><span class="sxs-lookup"><span data-stu-id="62d52-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="62d52-136">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="62d52-136">Example 2</span></span>

<span data-ttu-id="62d52-137">GRAVIDADE (2)</span><span class="sxs-lookup"><span data-stu-id="62d52-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="62d52-138">Retorna 180 graus, porque 2 radianos fica entre 90 e 270 graus.</span><span class="sxs-lookup"><span data-stu-id="62d52-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="62d52-139">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="62d52-139">Example 3</span></span>

<span data-ttu-id="62d52-140">GRAVITY(100 graus, 110 graus, 290 graus)</span><span class="sxs-lookup"><span data-stu-id="62d52-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="62d52-141">Retorna 0 grau.</span><span class="sxs-lookup"><span data-stu-id="62d52-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="62d52-142">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="62d52-142">Example 4</span></span>

<span data-ttu-id="62d52-143">GRAVITY(100 graus, 290 graus, 110 graus)</span><span class="sxs-lookup"><span data-stu-id="62d52-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="62d52-144">Retorna 0 grau.</span><span class="sxs-lookup"><span data-stu-id="62d52-144">Returns 0 degrees.</span></span>
  

