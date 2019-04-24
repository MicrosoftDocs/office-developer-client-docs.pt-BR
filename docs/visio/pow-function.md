---
title: Função POW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Retorna um número elevado à potência de um expoente.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356046"
---
# <a name="pow-function"></a><span data-ttu-id="e91e4-103">Função POW</span><span class="sxs-lookup"><span data-stu-id="e91e4-103">POW Function</span></span>

<span data-ttu-id="e91e4-104">Retorna um número elevado à potência de um expoente.</span><span class="sxs-lookup"><span data-stu-id="e91e4-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e91e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e91e4-105">Syntax</span></span>

<span data-ttu-id="e91e4-106">POW (\* \* *número* \* \*, \* \* *expoente* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e91e4-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e91e4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e91e4-107">Parameters</span></span>

|<span data-ttu-id="e91e4-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e91e4-108">**Name**</span></span>|<span data-ttu-id="e91e4-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="e91e4-109">**Required/Optional**</span></span>|<span data-ttu-id="e91e4-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e91e4-110">**Data Type**</span></span>|<span data-ttu-id="e91e4-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e91e4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e91e4-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e91e4-112">_number_</span></span> <br/> |<span data-ttu-id="e91e4-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e91e4-113">Required</span></span>  <br/> |<span data-ttu-id="e91e4-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="e91e4-114">**Number**</span></span> <br/> |<span data-ttu-id="e91e4-115">O número a ser elevada a potência de um expoente.</span><span class="sxs-lookup"><span data-stu-id="e91e4-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="e91e4-116">_expoente_</span><span class="sxs-lookup"><span data-stu-id="e91e4-116">_exponent_</span></span> <br/> |<span data-ttu-id="e91e4-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e91e4-117">Required</span></span>  <br/> |<span data-ttu-id="e91e4-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="e91e4-118">**Number**</span></span> <br/> |<span data-ttu-id="e91e4-119">O expoente.</span><span class="sxs-lookup"><span data-stu-id="e91e4-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e91e4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e91e4-120">Remarks</span></span>

<span data-ttu-id="e91e4-121">Tanto o _número_ quanto o _expoente_ podem ser não inteiros e podem ser negativos.</span><span class="sxs-lookup"><span data-stu-id="e91e4-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="e91e4-122">Se _núm_ não for 0 e _expoente_ for 0, essa função retornará 1.</span><span class="sxs-lookup"><span data-stu-id="e91e4-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="e91e4-123">Se _núm_ for 0 e _expoente_ for negativo, essa função retornará 0,0.</span><span class="sxs-lookup"><span data-stu-id="e91e4-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="e91e4-124">Se _núm_ e _expoente_ forem 0, ou se _núm_ for negativo e _expoente_ não for um inteiro, essa função retornará 0,0.</span><span class="sxs-lookup"><span data-stu-id="e91e4-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="e91e4-125">Se tanto _núm_ quanto _expoente_ forem negativos, essa função retornará-1. #IND.</span><span class="sxs-lookup"><span data-stu-id="e91e4-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e91e4-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e91e4-126">Example</span></span>

<span data-ttu-id="e91e4-127">POW (5, 2)</span><span class="sxs-lookup"><span data-stu-id="e91e4-127">POW(5,2)</span></span> 
  
<span data-ttu-id="e91e4-128">Retornará 25.</span><span class="sxs-lookup"><span data-stu-id="e91e4-128">Returns 25.</span></span> 
  

