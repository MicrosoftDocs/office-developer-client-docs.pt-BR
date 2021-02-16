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
description: Retorna o tempo representado por hora, minuto e segundo.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414470"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="00524-103">Função TIME (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="00524-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="00524-104">Retorna o tempo representado por _hora,_ _minuto_ e _segundo._</span><span class="sxs-lookup"><span data-stu-id="00524-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="00524-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00524-105">Syntax</span></span>

<span data-ttu-id="00524-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span><span class="sxs-lookup"><span data-stu-id="00524-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00524-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00524-107">Parameters</span></span>

|<span data-ttu-id="00524-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="00524-108">**Name**</span></span>|<span data-ttu-id="00524-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="00524-109">**Required/Optional**</span></span>|<span data-ttu-id="00524-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="00524-110">**Data Type**</span></span>|<span data-ttu-id="00524-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="00524-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00524-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="00524-112">_hour_</span></span> <br/> |<span data-ttu-id="00524-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="00524-113">Required</span></span>  <br/> |<span data-ttu-id="00524-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="00524-114">**Numeric**</span></span> <br/> |<span data-ttu-id="00524-115">O componente de hora.</span><span class="sxs-lookup"><span data-stu-id="00524-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="00524-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="00524-116">_minute_</span></span> <br/> |<span data-ttu-id="00524-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="00524-117">Required</span></span>  <br/> |<span data-ttu-id="00524-118">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="00524-118">**Numeric**</span></span> <br/> |<span data-ttu-id="00524-119">O componente de minuto.</span><span class="sxs-lookup"><span data-stu-id="00524-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="00524-120">_segundo_</span><span class="sxs-lookup"><span data-stu-id="00524-120">_second_</span></span> <br/> |<span data-ttu-id="00524-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="00524-121">Required</span></span>  <br/> |<span data-ttu-id="00524-122">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="00524-122">**Numeric**</span></span> <br/> |<span data-ttu-id="00524-123">O componente de segundo.</span><span class="sxs-lookup"><span data-stu-id="00524-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00524-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="00524-124">Return value</span></span>

<span data-ttu-id="00524-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="00524-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="00524-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00524-126">Example 1</span></span>

<span data-ttu-id="00524-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="00524-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="00524-128">Retornará o valor que representa 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="00524-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="00524-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00524-129">Example 2</span></span>

<span data-ttu-id="00524-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="00524-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="00524-131">Retornará o valor que representa 15:30.</span><span class="sxs-lookup"><span data-stu-id="00524-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="00524-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="00524-132">Example 3</span></span>

<span data-ttu-id="00524-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="00524-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="00524-134">Retornará o valor que representa 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="00524-134">Returns the value representing 23:30:30.</span></span>
  

