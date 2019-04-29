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
description: Retorna a magnitude do vetor cujo aumento é A e cuja execução é B, multiplicada pelas constantes constantA e constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420455"
---
# <a name="magnitude-function"></a><span data-ttu-id="5a049-103">Função MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="5a049-103">MAGNITUDE Function</span></span>

<span data-ttu-id="5a049-104">Retorna a magnitude do vetor cujo aumento é _a_ e cuja execução é _B_, multiplicada pelas constantes _constantA_ e _constantB_.</span><span class="sxs-lookup"><span data-stu-id="5a049-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5a049-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a049-105">Syntax</span></span>

<span data-ttu-id="5a049-106">MAGNITUDE (\* \* *constantA* \* \*, \* \* *A* \* \*, \* \* *constantB* \* \*, \* \* *B* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5a049-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5a049-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a049-107">Parameters</span></span>

|<span data-ttu-id="5a049-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5a049-108">**Name**</span></span>|<span data-ttu-id="5a049-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="5a049-109">**Required/Optional**</span></span>|<span data-ttu-id="5a049-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5a049-110">**Data Type**</span></span>|<span data-ttu-id="5a049-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a049-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5a049-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="5a049-112">_constantA_</span></span> <br/> |<span data-ttu-id="5a049-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5a049-113">Required</span></span>  <br/> |<span data-ttu-id="5a049-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="5a049-114">**Number**</span></span> <br/> |<span data-ttu-id="5a049-115">A constante pela qual multiplicar a elevação.</span><span class="sxs-lookup"><span data-stu-id="5a049-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="5a049-116">_A_</span><span class="sxs-lookup"><span data-stu-id="5a049-116">_A_</span></span> <br/> |<span data-ttu-id="5a049-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5a049-117">Required</span></span>  <br/> |<span data-ttu-id="5a049-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="5a049-118">**Number**</span></span> <br/> |<span data-ttu-id="5a049-119">A elevação.</span><span class="sxs-lookup"><span data-stu-id="5a049-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="5a049-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="5a049-120">_constantB_</span></span> <br/> |<span data-ttu-id="5a049-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5a049-121">Required</span></span>  <br/> |<span data-ttu-id="5a049-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="5a049-122">**Number**</span></span> <br/> |<span data-ttu-id="5a049-123">A constante pela qual multiplicar a execução.</span><span class="sxs-lookup"><span data-stu-id="5a049-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="5a049-124">_A.b.c._</span><span class="sxs-lookup"><span data-stu-id="5a049-124">_B_</span></span> <br/> |<span data-ttu-id="5a049-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5a049-125">Required</span></span>  <br/> |<span data-ttu-id="5a049-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="5a049-126">**Number**</span></span> <br/> |<span data-ttu-id="5a049-127">A execução.</span><span class="sxs-lookup"><span data-stu-id="5a049-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a049-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a049-128">Remarks</span></span>

<span data-ttu-id="5a049-129">MAGNITUDE é calculada de acordo com a fórmula a seguir:</span><span class="sxs-lookup"><span data-stu-id="5a049-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="5a049-130">SQRT ((constantA \* A) ^ 2 + (constantB \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="5a049-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="5a049-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5a049-131">Example</span></span>

<span data-ttu-id="5a049-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="5a049-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="5a049-133">Retornará 5.</span><span class="sxs-lookup"><span data-stu-id="5a049-133">Returns 5.</span></span> 
  

