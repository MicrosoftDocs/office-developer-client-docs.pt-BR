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
description: Retorna valueiftrue se logicalexpression for TRUE. Caso contrário, ele retornará valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405468"
---
# <a name="if-function"></a><span data-ttu-id="07f8c-104">Função IF</span><span class="sxs-lookup"><span data-stu-id="07f8c-104">IF Function</span></span>

<span data-ttu-id="07f8c-105">Retorna  _valueiftrue_ se  _logicalexpression_ for TRUE.</span><span class="sxs-lookup"><span data-stu-id="07f8c-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="07f8c-106">Caso contrário, ele  _retornará valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="07f8c-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="07f8c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07f8c-107">Syntax</span></span>

<span data-ttu-id="07f8c-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span><span class="sxs-lookup"><span data-stu-id="07f8c-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="07f8c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07f8c-109">Parameters</span></span>

|<span data-ttu-id="07f8c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="07f8c-110">**Name**</span></span>|<span data-ttu-id="07f8c-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="07f8c-111">**Required/Optional**</span></span>|<span data-ttu-id="07f8c-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="07f8c-112">**Data Type**</span></span>|<span data-ttu-id="07f8c-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="07f8c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="07f8c-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="07f8c-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="07f8c-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="07f8c-115">Required</span></span>  <br/> |<span data-ttu-id="07f8c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="07f8c-116">**String**</span></span> <br/> |<span data-ttu-id="07f8c-117">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="07f8c-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="07f8c-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="07f8c-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="07f8c-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="07f8c-119">Required</span></span>  <br/> |<span data-ttu-id="07f8c-120">**Varia**</span><span class="sxs-lookup"><span data-stu-id="07f8c-120">**Varies**</span></span> <br/> |<span data-ttu-id="07f8c-121">Valor a ser retornada  _se expressão lógica_ for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="07f8c-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="07f8c-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="07f8c-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="07f8c-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="07f8c-123">Required</span></span>  <br/> |<span data-ttu-id="07f8c-124">**Varia**</span><span class="sxs-lookup"><span data-stu-id="07f8c-124">**Varies**</span></span> <br/> | <span data-ttu-id="07f8c-125">Valor a ser retornada  _se expressão lógica_ for false.</span><span class="sxs-lookup"><span data-stu-id="07f8c-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="07f8c-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="07f8c-126">Return value</span></span>

<span data-ttu-id="07f8c-127">Várias</span><span class="sxs-lookup"><span data-stu-id="07f8c-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="07f8c-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="07f8c-128">Example</span></span>

<span data-ttu-id="07f8c-129">IF(Height \> 1,25 in,5,7)</span><span class="sxs-lookup"><span data-stu-id="07f8c-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="07f8c-130">Retorna 5 se a altura da forma for maior que 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="07f8c-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="07f8c-131">Retorna 7 se a altura da forma for menor que ou igual a 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="07f8c-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

