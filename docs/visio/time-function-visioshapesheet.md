---
title: Função TIME (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Retorna a hora representada por hora, minuto e segundo.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414470"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="22f68-103">Função TIME (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="22f68-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="22f68-104">Retorna a hora representada por _hora_, _minuto_e _segundo_.</span><span class="sxs-lookup"><span data-stu-id="22f68-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="22f68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22f68-105">Syntax</span></span>

<span data-ttu-id="22f68-106">HORA (\* \* *hora* \* \*, \* \* *minuto* \* \*, \* \* *segundo* \* \*)</span><span class="sxs-lookup"><span data-stu-id="22f68-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="22f68-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22f68-107">Parameters</span></span>

|<span data-ttu-id="22f68-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="22f68-108">**Name**</span></span>|<span data-ttu-id="22f68-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="22f68-109">**Required/Optional**</span></span>|<span data-ttu-id="22f68-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="22f68-110">**Data Type**</span></span>|<span data-ttu-id="22f68-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="22f68-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="22f68-112">_hora_</span><span class="sxs-lookup"><span data-stu-id="22f68-112">_hour_</span></span> <br/> |<span data-ttu-id="22f68-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="22f68-113">Required</span></span>  <br/> |<span data-ttu-id="22f68-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="22f68-114">**Numeric**</span></span> <br/> |<span data-ttu-id="22f68-115">O componente de hora.</span><span class="sxs-lookup"><span data-stu-id="22f68-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="22f68-116">_inclusões_</span><span class="sxs-lookup"><span data-stu-id="22f68-116">_minute_</span></span> <br/> |<span data-ttu-id="22f68-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="22f68-117">Required</span></span>  <br/> |<span data-ttu-id="22f68-118">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="22f68-118">**Numeric**</span></span> <br/> |<span data-ttu-id="22f68-119">O componente de minuto.</span><span class="sxs-lookup"><span data-stu-id="22f68-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="22f68-120">_secundária_</span><span class="sxs-lookup"><span data-stu-id="22f68-120">_second_</span></span> <br/> |<span data-ttu-id="22f68-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="22f68-121">Required</span></span>  <br/> |<span data-ttu-id="22f68-122">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="22f68-122">**Numeric**</span></span> <br/> |<span data-ttu-id="22f68-123">O componente de segundo.</span><span class="sxs-lookup"><span data-stu-id="22f68-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="22f68-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="22f68-124">Return value</span></span>

<span data-ttu-id="22f68-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="22f68-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="22f68-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22f68-126">Example 1</span></span>

<span data-ttu-id="22f68-127">TEMPO (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="22f68-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="22f68-128">Retornará o valor que representa 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="22f68-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="22f68-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22f68-129">Example 2</span></span>

<span data-ttu-id="22f68-130">FORMATO (tempo (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="22f68-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="22f68-131">Retornará o valor que representa 15:30.</span><span class="sxs-lookup"><span data-stu-id="22f68-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="22f68-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="22f68-132">Example 3</span></span>

<span data-ttu-id="22f68-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="22f68-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="22f68-134">Retornará o valor que representa 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="22f68-134">Returns the value representing 23:30:30.</span></span>
  

