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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405468"
---
# <a name="if-function"></a><span data-ttu-id="aaa80-104">Função IF</span><span class="sxs-lookup"><span data-stu-id="aaa80-104">IF Function</span></span>

<span data-ttu-id="aaa80-105">Retorna _valueiftrue_ se _logicaly_ for true.</span><span class="sxs-lookup"><span data-stu-id="aaa80-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="aaa80-106">Caso contrário, retornará _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="aaa80-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aaa80-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaa80-107">Syntax</span></span>

<span data-ttu-id="aaa80-108">IF (\* \* *LogicalName* \* \*, \* \* *valueiftrue* \* \*, \* \* *valueiffalse* \* \*)</span><span class="sxs-lookup"><span data-stu-id="aaa80-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aaa80-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaa80-109">Parameters</span></span>

|<span data-ttu-id="aaa80-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="aaa80-110">**Name**</span></span>|<span data-ttu-id="aaa80-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="aaa80-111">**Required/Optional**</span></span>|<span data-ttu-id="aaa80-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="aaa80-112">**Data Type**</span></span>|<span data-ttu-id="aaa80-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aaa80-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aaa80-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="aaa80-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="aaa80-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aaa80-115">Required</span></span>  <br/> |<span data-ttu-id="aaa80-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aaa80-116">**String**</span></span> <br/> |<span data-ttu-id="aaa80-117">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="aaa80-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="aaa80-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="aaa80-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="aaa80-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aaa80-119">Required</span></span>  <br/> |<span data-ttu-id="aaa80-120">**Vai**</span><span class="sxs-lookup"><span data-stu-id="aaa80-120">**Varies**</span></span> <br/> |<span data-ttu-id="aaa80-121">Valor a ser retornado __ se logicalid for true.</span><span class="sxs-lookup"><span data-stu-id="aaa80-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="aaa80-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="aaa80-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="aaa80-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aaa80-123">Required</span></span>  <br/> |<span data-ttu-id="aaa80-124">**Vai**</span><span class="sxs-lookup"><span data-stu-id="aaa80-124">**Varies**</span></span> <br/> | <span data-ttu-id="aaa80-125">Valor a ser retornado __ se logicalid for false.</span><span class="sxs-lookup"><span data-stu-id="aaa80-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aaa80-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aaa80-126">Return value</span></span>

<span data-ttu-id="aaa80-127">Várias</span><span class="sxs-lookup"><span data-stu-id="aaa80-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="aaa80-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="aaa80-128">Example</span></span>

<span data-ttu-id="aaa80-129">SE (altura \> 1,25, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="aaa80-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="aaa80-130">Retorna 5 se a altura da forma for maior que 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="aaa80-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="aaa80-131">Retorna 7 se a altura da forma for menor que ou igual a 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="aaa80-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

