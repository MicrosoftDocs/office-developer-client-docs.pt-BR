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
description: Retorna a magnitude do vetor cuja elevação é A e cujo fluxo é B, multiplicado pelas constantes respectivas constantA e constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420455"
---
# <a name="magnitude-function"></a><span data-ttu-id="33ebd-103">Função MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="33ebd-103">MAGNITUDE Function</span></span>

<span data-ttu-id="33ebd-104">Retorna a magnitude do vetor cuja elevação é  _A_ e cujo fluxo é  _B_, multiplicado pelas constantes  _respectivas constantA_ e  _constantB_.</span><span class="sxs-lookup"><span data-stu-id="33ebd-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="33ebd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33ebd-105">Syntax</span></span>

<span data-ttu-id="33ebd-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span><span class="sxs-lookup"><span data-stu-id="33ebd-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="33ebd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33ebd-107">Parameters</span></span>

|<span data-ttu-id="33ebd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="33ebd-108">**Name**</span></span>|<span data-ttu-id="33ebd-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="33ebd-109">**Required/Optional**</span></span>|<span data-ttu-id="33ebd-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="33ebd-110">**Data Type**</span></span>|<span data-ttu-id="33ebd-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="33ebd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="33ebd-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="33ebd-112">_constantA_</span></span> <br/> |<span data-ttu-id="33ebd-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33ebd-113">Required</span></span>  <br/> |<span data-ttu-id="33ebd-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="33ebd-114">**Number**</span></span> <br/> |<span data-ttu-id="33ebd-115">A constante pela qual multiplicar a elevação.</span><span class="sxs-lookup"><span data-stu-id="33ebd-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="33ebd-116">_A_</span><span class="sxs-lookup"><span data-stu-id="33ebd-116">_A_</span></span> <br/> |<span data-ttu-id="33ebd-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33ebd-117">Required</span></span>  <br/> |<span data-ttu-id="33ebd-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="33ebd-118">**Number**</span></span> <br/> |<span data-ttu-id="33ebd-119">A elevação.</span><span class="sxs-lookup"><span data-stu-id="33ebd-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="33ebd-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="33ebd-120">_constantB_</span></span> <br/> |<span data-ttu-id="33ebd-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33ebd-121">Required</span></span>  <br/> |<span data-ttu-id="33ebd-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="33ebd-122">**Number**</span></span> <br/> |<span data-ttu-id="33ebd-123">A constante pela qual multiplicar a execução.</span><span class="sxs-lookup"><span data-stu-id="33ebd-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="33ebd-124">_B_</span><span class="sxs-lookup"><span data-stu-id="33ebd-124">_B_</span></span> <br/> |<span data-ttu-id="33ebd-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33ebd-125">Required</span></span>  <br/> |<span data-ttu-id="33ebd-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="33ebd-126">**Number**</span></span> <br/> |<span data-ttu-id="33ebd-127">A execução.</span><span class="sxs-lookup"><span data-stu-id="33ebd-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33ebd-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="33ebd-128">Remarks</span></span>

<span data-ttu-id="33ebd-129">MAGNITUDE é calculada de acordo com a fórmula a seguir:</span><span class="sxs-lookup"><span data-stu-id="33ebd-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="33ebd-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span><span class="sxs-lookup"><span data-stu-id="33ebd-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="33ebd-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="33ebd-131">Example</span></span>

<span data-ttu-id="33ebd-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="33ebd-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="33ebd-133">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="33ebd-133">Returns 5.</span></span> 
  

