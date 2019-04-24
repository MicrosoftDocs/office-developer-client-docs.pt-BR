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
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341486"
---
# <a name="ang360-function"></a><span data-ttu-id="6f6cf-103">Função ANG360</span><span class="sxs-lookup"><span data-stu-id="6f6cf-103">ANG360 Function</span></span>

<span data-ttu-id="6f6cf-104">Normaliza o intervalo de um ângulo para ser 0 \<= resultado \< 2PI radianos (0 \<= resultado \< 360 graus).</span><span class="sxs-lookup"><span data-stu-id="6f6cf-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6f6cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f6cf-105">Syntax</span></span>

<span data-ttu-id="6f6cf-106">ANG360 (\* \* *Angle* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6f6cf-106">ANG360(\*\* *angle* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6f6cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f6cf-107">Parameters</span></span>

|<span data-ttu-id="6f6cf-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6f6cf-108">**Name**</span></span>|<span data-ttu-id="6f6cf-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="6f6cf-109">**Required/Optional**</span></span>|<span data-ttu-id="6f6cf-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6f6cf-110">**Data Type**</span></span>|<span data-ttu-id="6f6cf-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f6cf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f6cf-112">_reto_</span><span class="sxs-lookup"><span data-stu-id="6f6cf-112">_angle_</span></span> <br/> |<span data-ttu-id="6f6cf-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6f6cf-113">Required</span></span>  <br/> |<span data-ttu-id="6f6cf-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="6f6cf-114">**Numeric**</span></span> <br/> |<span data-ttu-id="6f6cf-115">O ângulo a ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="6f6cf-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f6cf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f6cf-116">Remarks</span></span>

<span data-ttu-id="6f6cf-117">Se *Angle* não for especificado usando unidades angulares, será interpretado como radianos.</span><span class="sxs-lookup"><span data-stu-id="6f6cf-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="6f6cf-118">Se o *ângulo* não puder ser convertido em um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6f6cf-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="6f6cf-119">será retornado.</span><span class="sxs-lookup"><span data-stu-id="6f6cf-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6f6cf-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f6cf-120">Example 1</span></span>

<span data-ttu-id="6f6cf-121">ANG360(395 graus)</span><span class="sxs-lookup"><span data-stu-id="6f6cf-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="6f6cf-122">Retorna 35 graus</span><span class="sxs-lookup"><span data-stu-id="6f6cf-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6f6cf-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f6cf-123">Example 2</span></span>

<span data-ttu-id="6f6cf-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="6f6cf-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="6f6cf-125">Retorna 2,7664 rad.</span><span class="sxs-lookup"><span data-stu-id="6f6cf-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6f6cf-126">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6f6cf-126">Example 3</span></span>

<span data-ttu-id="6f6cf-127">ANG360 (45)</span><span class="sxs-lookup"><span data-stu-id="6f6cf-127">ANG360(45)</span></span>
  
<span data-ttu-id="6f6cf-128">Retorna 58,31 graus (1,0177 rad).</span><span class="sxs-lookup"><span data-stu-id="6f6cf-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

