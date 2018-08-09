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
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773159"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="33074-103">Função TIME (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="33074-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="33074-104">Retorna a hora representada por _hora_, _minuto_e _segundo_.</span><span class="sxs-lookup"><span data-stu-id="33074-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="33074-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33074-105">Syntax</span></span>

<span data-ttu-id="33074-106">TEMPO (* * *hora* * *, * * *minuto* * *, * * *segundo* * *)</span><span class="sxs-lookup"><span data-stu-id="33074-106">TIME(** *hour* **, ** *minute* **, ** *second* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="33074-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33074-107">Parameters</span></span>

|<span data-ttu-id="33074-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="33074-108">**Name**</span></span>|<span data-ttu-id="33074-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="33074-109">**Required/Optional**</span></span>|<span data-ttu-id="33074-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="33074-110">**Data Type**</span></span>|<span data-ttu-id="33074-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="33074-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="33074-112">_hora_</span><span class="sxs-lookup"><span data-stu-id="33074-112">_hour_</span></span> <br/> |<span data-ttu-id="33074-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33074-113">Required</span></span>  <br/> |<span data-ttu-id="33074-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="33074-114">**Numeric**</span></span> <br/> |<span data-ttu-id="33074-115">O componente de hora.</span><span class="sxs-lookup"><span data-stu-id="33074-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="33074-116">_minuto_</span><span class="sxs-lookup"><span data-stu-id="33074-116">_minute_</span></span> <br/> |<span data-ttu-id="33074-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33074-117">Required</span></span>  <br/> |<span data-ttu-id="33074-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="33074-118">**Numeric**</span></span> <br/> |<span data-ttu-id="33074-119">O componente de minuto.</span><span class="sxs-lookup"><span data-stu-id="33074-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="33074-120">_segundo_</span><span class="sxs-lookup"><span data-stu-id="33074-120">_second_</span></span> <br/> |<span data-ttu-id="33074-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33074-121">Required</span></span>  <br/> |<span data-ttu-id="33074-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="33074-122">**Numeric**</span></span> <br/> |<span data-ttu-id="33074-123">O componente de segundo.</span><span class="sxs-lookup"><span data-stu-id="33074-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="33074-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="33074-124">Return value</span></span>

<span data-ttu-id="33074-125">Numérico</span><span class="sxs-lookup"><span data-stu-id="33074-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="33074-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33074-126">Example 1</span></span>

<span data-ttu-id="33074-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="33074-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="33074-128">Retornará o valor que representa 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="33074-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="33074-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="33074-129">Example 2</span></span>

<span data-ttu-id="33074-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="33074-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="33074-131">Retornará o valor que representa 15:30.</span><span class="sxs-lookup"><span data-stu-id="33074-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="33074-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="33074-132">Example 3</span></span>

<span data-ttu-id="33074-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="33074-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="33074-134">Retornará o valor que representa 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="33074-134">Returns the value representing 23:30:30.</span></span>
  

