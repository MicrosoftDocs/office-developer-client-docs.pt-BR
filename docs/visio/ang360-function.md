---
title: Função ANG360
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normaliza o intervalo de um ângulo.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771259"
---
# <a name="ang360-function"></a><span data-ttu-id="f431d-103">Função ANG360</span><span class="sxs-lookup"><span data-stu-id="f431d-103">ANG360 Function</span></span>

<span data-ttu-id="f431d-104">Normaliza o intervalo de um ângulo para ser 0 \<= resultado \< 2PI radianos (0 \<= resultado \< 360 graus).</span><span class="sxs-lookup"><span data-stu-id="f431d-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f431d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f431d-105">Syntax</span></span>

<span data-ttu-id="f431d-106">ANG360 (* * *ângulo* * *)</span><span class="sxs-lookup"><span data-stu-id="f431d-106">ANG360(** *angle* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f431d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f431d-107">Parameters</span></span>

|<span data-ttu-id="f431d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f431d-108">**Name**</span></span>|<span data-ttu-id="f431d-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f431d-109">**Required/Optional**</span></span>|<span data-ttu-id="f431d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f431d-110">**Data Type**</span></span>|<span data-ttu-id="f431d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f431d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f431d-112">_ângulo_</span><span class="sxs-lookup"><span data-stu-id="f431d-112">_angle_</span></span> <br/> |<span data-ttu-id="f431d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f431d-113">Required</span></span>  <br/> |<span data-ttu-id="f431d-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="f431d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="f431d-115">O ângulo a ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="f431d-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f431d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f431d-116">Remarks</span></span>

<span data-ttu-id="f431d-117">Se o *ângulo* não for especificado, usando as unidades angulares, ela será interpretada como radianos.</span><span class="sxs-lookup"><span data-stu-id="f431d-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="f431d-118">Se o *ângulo* não puder ser convertida para um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="f431d-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="f431d-119">erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="f431d-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f431d-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f431d-120">Example 1</span></span>

<span data-ttu-id="f431d-121">ANG360(395 graus)</span><span class="sxs-lookup"><span data-stu-id="f431d-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="f431d-122">Retorna 35 graus</span><span class="sxs-lookup"><span data-stu-id="f431d-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f431d-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f431d-123">Example 2</span></span>

<span data-ttu-id="f431d-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="f431d-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="f431d-125">Retorna 2,7664 rad.</span><span class="sxs-lookup"><span data-stu-id="f431d-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f431d-126">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f431d-126">Example 3</span></span>

<span data-ttu-id="f431d-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="f431d-127">ANG360(45)</span></span>
  
<span data-ttu-id="f431d-128">Retorna 58,31 graus (1,0177 rad).</span><span class="sxs-lookup"><span data-stu-id="f431d-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

