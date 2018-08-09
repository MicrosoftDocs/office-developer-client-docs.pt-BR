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
description: Retorna ValorSeVerdadeiro se logicalexpression for TRUE. Caso contrário, ele retorna ValorSeFalso.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772056"
---
# <a name="if-function"></a><span data-ttu-id="61200-104">Função IF</span><span class="sxs-lookup"><span data-stu-id="61200-104">IF Function</span></span>

<span data-ttu-id="61200-105">Retorna _ValorSeVerdadeiro_ se _logicalexpression_ for TRUE.</span><span class="sxs-lookup"><span data-stu-id="61200-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="61200-106">Caso contrário, ele retorna _ValorSeFalso_.</span><span class="sxs-lookup"><span data-stu-id="61200-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="61200-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61200-107">Syntax</span></span>

<span data-ttu-id="61200-108">IF (* * *logicalexpression* * *, * * *ValorSeVerdadeiro* * *, * * *ValorSeFalso* * *)</span><span class="sxs-lookup"><span data-stu-id="61200-108">IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61200-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61200-109">Parameters</span></span>

|<span data-ttu-id="61200-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="61200-110">**Name**</span></span>|<span data-ttu-id="61200-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="61200-111">**Required/Optional**</span></span>|<span data-ttu-id="61200-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="61200-112">**Data Type**</span></span>|<span data-ttu-id="61200-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="61200-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61200-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="61200-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="61200-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61200-115">Required</span></span>  <br/> |<span data-ttu-id="61200-116">**String**</span><span class="sxs-lookup"><span data-stu-id="61200-116">**String**</span></span> <br/> |<span data-ttu-id="61200-117">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="61200-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="61200-118">_ValorSeVerdadeiro_</span><span class="sxs-lookup"><span data-stu-id="61200-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="61200-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61200-119">Required</span></span>  <br/> |<span data-ttu-id="61200-120">**Varia**</span><span class="sxs-lookup"><span data-stu-id="61200-120">**Varies**</span></span> <br/> |<span data-ttu-id="61200-121">O valor retornado se _logicalexpression_ for true.</span><span class="sxs-lookup"><span data-stu-id="61200-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="61200-122">_ValorSeFalso_</span><span class="sxs-lookup"><span data-stu-id="61200-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="61200-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61200-123">Required</span></span>  <br/> |<span data-ttu-id="61200-124">**Varia**</span><span class="sxs-lookup"><span data-stu-id="61200-124">**Varies**</span></span> <br/> | <span data-ttu-id="61200-125">O valor retornado se _logicalexpression_ for falso.</span><span class="sxs-lookup"><span data-stu-id="61200-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="61200-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="61200-126">Return value</span></span>

<span data-ttu-id="61200-127">Varia</span><span class="sxs-lookup"><span data-stu-id="61200-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="61200-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="61200-128">Example</span></span>

<span data-ttu-id="61200-129">IF (altura \> 1,25 pol, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="61200-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="61200-p103">Retorna 5 se a altura da forma for maior que 1,25 polegadas. Retorna 7 se a altura da forma for menor que ou igual a 1,25 polegadas.</span><span class="sxs-lookup"><span data-stu-id="61200-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

