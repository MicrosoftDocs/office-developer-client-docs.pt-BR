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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280994"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="f9f8a-103">Função TIME (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="f9f8a-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="f9f8a-104">Retorna a hora representada por _hora_, _minuto_e _segundo_.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f9f8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9f8a-105">Syntax</span></span>

<span data-ttu-id="f9f8a-106">HORA (\* \* *hora* \* \*, \* \* *minuto* \* \*, \* \* *segundo* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f9f8a-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f9f8a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9f8a-107">Parameters</span></span>

|<span data-ttu-id="f9f8a-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-108">**Name**</span></span>|<span data-ttu-id="f9f8a-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-109">**Required/Optional**</span></span>|<span data-ttu-id="f9f8a-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-110">**Data Type**</span></span>|<span data-ttu-id="f9f8a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f9f8a-112">_hora_</span><span class="sxs-lookup"><span data-stu-id="f9f8a-112">_hour_</span></span> <br/> |<span data-ttu-id="f9f8a-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f9f8a-113">Required</span></span>  <br/> |<span data-ttu-id="f9f8a-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="f9f8a-115">O componente de hora.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="f9f8a-116">_inclusões_</span><span class="sxs-lookup"><span data-stu-id="f9f8a-116">_minute_</span></span> <br/> |<span data-ttu-id="f9f8a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f9f8a-117">Required</span></span>  <br/> |<span data-ttu-id="f9f8a-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-118">**Numeric**</span></span> <br/> |<span data-ttu-id="f9f8a-119">O componente de minuto.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="f9f8a-120">_secundária_</span><span class="sxs-lookup"><span data-stu-id="f9f8a-120">_second_</span></span> <br/> |<span data-ttu-id="f9f8a-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f9f8a-121">Required</span></span>  <br/> |<span data-ttu-id="f9f8a-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-122">**Numeric**</span></span> <br/> |<span data-ttu-id="f9f8a-123">O componente de segundo.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f9f8a-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f9f8a-124">Return value</span></span>

<span data-ttu-id="f9f8a-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="f9f8a-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="f9f8a-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9f8a-126">Example 1</span></span>

<span data-ttu-id="f9f8a-127">TEMPO (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="f9f8a-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="f9f8a-128">Retornará o valor que representa 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f9f8a-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f9f8a-129">Example 2</span></span>

<span data-ttu-id="f9f8a-130">FORMATO (tempo (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="f9f8a-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="f9f8a-131">Retornará o valor que representa 15:30.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f9f8a-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f9f8a-132">Example 3</span></span>

<span data-ttu-id="f9f8a-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="f9f8a-134">Retornará o valor que representa 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-134">Returns the value representing 23:30:30.</span></span>
  

