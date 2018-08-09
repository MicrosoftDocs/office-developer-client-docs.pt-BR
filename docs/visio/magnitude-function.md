---
title: Função MAGNITUDE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Retorna a magnitude do vetor cuja elevação é A e cuja execução é B, multiplicada pelas constantes constanteA e constanteB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772304"
---
# <a name="magnitude-function"></a><span data-ttu-id="375d8-103">Função MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="375d8-103">MAGNITUDE Function</span></span>

<span data-ttu-id="375d8-104">Retorna a magnitude do vetor cuja elevação é _A_ e cuja execução é _B_, multiplicada pelas respectivas constantes _constanteA_ e _constanteB_.</span><span class="sxs-lookup"><span data-stu-id="375d8-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="375d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="375d8-105">Syntax</span></span>

<span data-ttu-id="375d8-106">MAGNITUDE (* * *constanteA* * *, * * *uma* * *, * * *constanteB* * *, * * *B* * *)</span><span class="sxs-lookup"><span data-stu-id="375d8-106">MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="375d8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="375d8-107">Parameters</span></span>

|<span data-ttu-id="375d8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="375d8-108">**Name**</span></span>|<span data-ttu-id="375d8-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="375d8-109">**Required/Optional**</span></span>|<span data-ttu-id="375d8-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="375d8-110">**Data Type**</span></span>|<span data-ttu-id="375d8-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="375d8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="375d8-112">_constanteA_</span><span class="sxs-lookup"><span data-stu-id="375d8-112">_constantA_</span></span> <br/> |<span data-ttu-id="375d8-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="375d8-113">Required</span></span>  <br/> |<span data-ttu-id="375d8-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="375d8-114">**Number**</span></span> <br/> |<span data-ttu-id="375d8-115">A constante pela qual multiplicar a elevação.</span><span class="sxs-lookup"><span data-stu-id="375d8-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="375d8-116">_A_</span><span class="sxs-lookup"><span data-stu-id="375d8-116">_A_</span></span> <br/> |<span data-ttu-id="375d8-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="375d8-117">Required</span></span>  <br/> |<span data-ttu-id="375d8-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="375d8-118">**Number**</span></span> <br/> |<span data-ttu-id="375d8-119">A elevação.</span><span class="sxs-lookup"><span data-stu-id="375d8-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="375d8-120">_constanteB_</span><span class="sxs-lookup"><span data-stu-id="375d8-120">_constantB_</span></span> <br/> |<span data-ttu-id="375d8-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="375d8-121">Required</span></span>  <br/> |<span data-ttu-id="375d8-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="375d8-122">**Number**</span></span> <br/> |<span data-ttu-id="375d8-123">A constante pela qual multiplicar a execução.</span><span class="sxs-lookup"><span data-stu-id="375d8-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="375d8-124">_B_</span><span class="sxs-lookup"><span data-stu-id="375d8-124">_B_</span></span> <br/> |<span data-ttu-id="375d8-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="375d8-125">Required</span></span>  <br/> |<span data-ttu-id="375d8-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="375d8-126">**Number**</span></span> <br/> |<span data-ttu-id="375d8-127">A execução.</span><span class="sxs-lookup"><span data-stu-id="375d8-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="375d8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="375d8-128">Remarks</span></span>

<span data-ttu-id="375d8-129">MAGNITUDE é calculada de acordo com a fórmula a seguir:</span><span class="sxs-lookup"><span data-stu-id="375d8-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="375d8-130">SQRT ((constanteA \* uma) ^ 2 + (constanteB \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="375d8-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="375d8-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="375d8-131">Example</span></span>

<span data-ttu-id="375d8-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="375d8-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="375d8-133">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="375d8-133">Returns 5.</span></span> 
  

