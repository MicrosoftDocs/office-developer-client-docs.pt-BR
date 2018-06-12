---
title: Função ASIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é um número.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771300"
---
# <a name="asin-function"></a><span data-ttu-id="9aa71-103">Função ASIN</span><span class="sxs-lookup"><span data-stu-id="9aa71-103">ASIN Function</span></span>

<span data-ttu-id="9aa71-104">Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é um *número* .</span><span class="sxs-lookup"><span data-stu-id="9aa71-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9aa71-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa71-105">Syntax</span></span>

<span data-ttu-id="9aa71-106">ASIN (* * *número* * *)</span><span class="sxs-lookup"><span data-stu-id="9aa71-106">ASIN(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9aa71-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aa71-107">Parameters</span></span>

|<span data-ttu-id="9aa71-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9aa71-108">**Name**</span></span>|<span data-ttu-id="9aa71-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="9aa71-109">**Required/Optional**</span></span>|<span data-ttu-id="9aa71-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9aa71-110">**Data Type**</span></span>|<span data-ttu-id="9aa71-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9aa71-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9aa71-112">_number_</span><span class="sxs-lookup"><span data-stu-id="9aa71-112">_number_</span></span> <br/> |<span data-ttu-id="9aa71-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9aa71-113">Required</span></span>  <br/> |<span data-ttu-id="9aa71-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="9aa71-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9aa71-115">O seno do ângulo.</span><span class="sxs-lookup"><span data-stu-id="9aa71-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9aa71-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa71-116">Remarks</span></span>

<span data-ttu-id="9aa71-117">O valor de entrada deve estar no intervalo -1 < = *número* < = 1 ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="9aa71-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="9aa71-118">erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="9aa71-118">error is returned.</span></span> <span data-ttu-id="9aa71-119">O ângulo resultante está no intervalo -PI/2 < = *ângulo* < = PI/2 radianos (-90 < = *ângulo* < = 90 graus).</span><span class="sxs-lookup"><span data-stu-id="9aa71-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="9aa71-120">Example</span><span class="sxs-lookup"><span data-stu-id="9aa71-120">Example</span></span>

<span data-ttu-id="9aa71-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="9aa71-121">ASIN(1)</span></span>
  
<span data-ttu-id="9aa71-122">Retorna 90 graus</span><span class="sxs-lookup"><span data-stu-id="9aa71-122">Returns 90 deg</span></span>
  

