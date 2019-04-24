---
title: Função IF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Retorna valueiftrue se logicaly for TRUE. Caso contrário, retornará valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344762"
---
# <a name="if-function"></a><span data-ttu-id="e2375-104">Função IF</span><span class="sxs-lookup"><span data-stu-id="e2375-104">IF Function</span></span>

<span data-ttu-id="e2375-105">Retorna _valueiftrue_ se _logicaly_ for true.</span><span class="sxs-lookup"><span data-stu-id="e2375-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="e2375-106">Caso contrário, retornará _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="e2375-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e2375-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2375-107">Syntax</span></span>

<span data-ttu-id="e2375-108">IF (\* \* *LogicalName* \* \*, \* \* *valueiftrue* \* \*, \* \* *valueiffalse* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e2375-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e2375-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2375-109">Parameters</span></span>

|<span data-ttu-id="e2375-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e2375-110">**Name**</span></span>|<span data-ttu-id="e2375-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="e2375-111">**Required/Optional**</span></span>|<span data-ttu-id="e2375-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e2375-112">**Data Type**</span></span>|<span data-ttu-id="e2375-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2375-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e2375-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="e2375-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="e2375-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e2375-115">Required</span></span>  <br/> |<span data-ttu-id="e2375-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e2375-116">**String**</span></span> <br/> |<span data-ttu-id="e2375-117">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="e2375-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="e2375-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="e2375-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="e2375-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e2375-119">Required</span></span>  <br/> |<span data-ttu-id="e2375-120">**Vai**</span><span class="sxs-lookup"><span data-stu-id="e2375-120">**Varies**</span></span> <br/> |<span data-ttu-id="e2375-121">Valor a ser retornado __ se logicalid for true.</span><span class="sxs-lookup"><span data-stu-id="e2375-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="e2375-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="e2375-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="e2375-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e2375-123">Required</span></span>  <br/> |<span data-ttu-id="e2375-124">**Vai**</span><span class="sxs-lookup"><span data-stu-id="e2375-124">**Varies**</span></span> <br/> | <span data-ttu-id="e2375-125">Valor a ser retornado __ se logicalid for false.</span><span class="sxs-lookup"><span data-stu-id="e2375-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e2375-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e2375-126">Return value</span></span>

<span data-ttu-id="e2375-127">Várias</span><span class="sxs-lookup"><span data-stu-id="e2375-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="e2375-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e2375-128">Example</span></span>

<span data-ttu-id="e2375-129">SE (altura \> 1,25, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="e2375-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="e2375-130">Retorna 5 se a altura da forma for maior que 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="e2375-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="e2375-131">Retorna 7 se a altura da forma for menor que ou igual a 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="e2375-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

