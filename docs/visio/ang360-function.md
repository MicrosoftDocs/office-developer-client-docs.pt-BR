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
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160297"
---
# <a name="ang360-function"></a><span data-ttu-id="43747-103">Função ANG360</span><span class="sxs-lookup"><span data-stu-id="43747-103">ANG360 Function</span></span>

<span data-ttu-id="43747-104">Normaliza o intervalo de um ângulo para ser 0 \< = resultado \< 2PI radianos (0 \< = resultado \< 360 graus).</span><span class="sxs-lookup"><span data-stu-id="43747-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="43747-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43747-105">Syntax</span></span>

<span data-ttu-id="43747-106">ANG360 (***ângulo*** )</span><span class="sxs-lookup"><span data-stu-id="43747-106">ANG360(***angle*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="43747-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43747-107">Parameters</span></span>

|<span data-ttu-id="43747-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="43747-108">**Name**</span></span>|<span data-ttu-id="43747-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="43747-109">**Required/Optional**</span></span>|<span data-ttu-id="43747-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="43747-110">**Data Type**</span></span>|<span data-ttu-id="43747-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43747-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="43747-112">_ângulo_</span><span class="sxs-lookup"><span data-stu-id="43747-112">_angle_</span></span> <br/> |<span data-ttu-id="43747-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="43747-113">Required</span></span>  <br/> |<span data-ttu-id="43747-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="43747-114">**Numeric**</span></span> <br/> |<span data-ttu-id="43747-115">O ângulo a ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="43747-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43747-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="43747-116">Remarks</span></span>

<span data-ttu-id="43747-117">Se *Angle* não for especificado usando unidades angulares, será interpretado como radianos.</span><span class="sxs-lookup"><span data-stu-id="43747-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="43747-118">Se o *ângulo* não puder ser convertido em um valor, um #VALUE!</span><span class="sxs-lookup"><span data-stu-id="43747-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="43747-119">será retornado.</span><span class="sxs-lookup"><span data-stu-id="43747-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="43747-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43747-120">Example 1</span></span>

<span data-ttu-id="43747-121">ANG360(395 graus)</span><span class="sxs-lookup"><span data-stu-id="43747-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="43747-122">Retorna 35 graus</span><span class="sxs-lookup"><span data-stu-id="43747-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="43747-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="43747-123">Example 2</span></span>

<span data-ttu-id="43747-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="43747-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="43747-125">Retorna 2,7664 rad.</span><span class="sxs-lookup"><span data-stu-id="43747-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="43747-126">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="43747-126">Example 3</span></span>

<span data-ttu-id="43747-127">ANG360 (45)</span><span class="sxs-lookup"><span data-stu-id="43747-127">ANG360(45)</span></span>
  
<span data-ttu-id="43747-128">Retorna 58,31 graus (1,0177 rad).</span><span class="sxs-lookup"><span data-stu-id="43747-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

