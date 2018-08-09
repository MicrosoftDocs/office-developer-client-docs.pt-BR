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
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772593"
---
# <a name="pow-function"></a><span data-ttu-id="eb045-103">Função POW</span><span class="sxs-lookup"><span data-stu-id="eb045-103">POW Function</span></span>

<span data-ttu-id="eb045-104">Retorna um número elevado à potência de um expoente.</span><span class="sxs-lookup"><span data-stu-id="eb045-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eb045-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb045-105">Syntax</span></span>

<span data-ttu-id="eb045-106">POW (* * *número* * *, * * *expoente* * *)</span><span class="sxs-lookup"><span data-stu-id="eb045-106">POW(** *number* **, ** *exponent* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eb045-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb045-107">Parameters</span></span>

|<span data-ttu-id="eb045-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="eb045-108">**Name**</span></span>|<span data-ttu-id="eb045-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="eb045-109">**Required/Optional**</span></span>|<span data-ttu-id="eb045-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="eb045-110">**Data Type**</span></span>|<span data-ttu-id="eb045-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eb045-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eb045-112">_number_</span><span class="sxs-lookup"><span data-stu-id="eb045-112">_number_</span></span> <br/> |<span data-ttu-id="eb045-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="eb045-113">Required</span></span>  <br/> |<span data-ttu-id="eb045-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="eb045-114">**Number**</span></span> <br/> |<span data-ttu-id="eb045-115">O número a ser elevada a potência de um expoente.</span><span class="sxs-lookup"><span data-stu-id="eb045-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="eb045-116">_expoente_</span><span class="sxs-lookup"><span data-stu-id="eb045-116">_exponent_</span></span> <br/> |<span data-ttu-id="eb045-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="eb045-117">Required</span></span>  <br/> |<span data-ttu-id="eb045-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="eb045-118">**Number**</span></span> <br/> |<span data-ttu-id="eb045-119">O expoente.</span><span class="sxs-lookup"><span data-stu-id="eb045-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb045-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb045-120">Remarks</span></span>

<span data-ttu-id="eb045-121">_Número_ e o _expoente_ podem ser não-inteiros e devem ser negativos.</span><span class="sxs-lookup"><span data-stu-id="eb045-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="eb045-122">Se _Núm_ não for 0 e o _expoente_ é 0, essa função retornará 1.</span><span class="sxs-lookup"><span data-stu-id="eb045-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="eb045-123">Se _Núm_ for 0 e o _expoente_ for negativo, essa função retornará 0,0.</span><span class="sxs-lookup"><span data-stu-id="eb045-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="eb045-124">Se o _número_ e o _expoente_ vão de 0 ou se _Núm_ for negativo e _expoente_ não for um inteiro, essa função retornará 0,0.</span><span class="sxs-lookup"><span data-stu-id="eb045-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="eb045-125">Se o _número_ e o _expoente_ forem negativos, essa função retornará -1. #IND.</span><span class="sxs-lookup"><span data-stu-id="eb045-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="eb045-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eb045-126">Example</span></span>

<span data-ttu-id="eb045-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="eb045-127">POW(5,2)</span></span> 
  
<span data-ttu-id="eb045-128">Retornará 25.</span><span class="sxs-lookup"><span data-stu-id="eb045-128">Returns 25.</span></span> 
  

