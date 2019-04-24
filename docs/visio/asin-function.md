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
description: Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é núm.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341521"
---
# <a name="asin-function"></a><span data-ttu-id="9b66c-103">Função ASIN</span><span class="sxs-lookup"><span data-stu-id="9b66c-103">ASIN Function</span></span>

<span data-ttu-id="9b66c-104">Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é *núm* .</span><span class="sxs-lookup"><span data-stu-id="9b66c-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9b66c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b66c-105">Syntax</span></span>

<span data-ttu-id="9b66c-106">Asen (\* \* *número* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9b66c-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9b66c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b66c-107">Parameters</span></span>

|<span data-ttu-id="9b66c-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9b66c-108">**Name**</span></span>|<span data-ttu-id="9b66c-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="9b66c-109">**Required/Optional**</span></span>|<span data-ttu-id="9b66c-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9b66c-110">**Data Type**</span></span>|<span data-ttu-id="9b66c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9b66c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9b66c-112">_number_</span><span class="sxs-lookup"><span data-stu-id="9b66c-112">_number_</span></span> <br/> |<span data-ttu-id="9b66c-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9b66c-113">Required</span></span>  <br/> |<span data-ttu-id="9b66c-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="9b66c-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9b66c-115">O seno do ângulo.</span><span class="sxs-lookup"><span data-stu-id="9b66c-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b66c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b66c-116">Remarks</span></span>

<span data-ttu-id="9b66c-117">O valor de entrada deve estar no intervalo-1 < = *Number* < = 1, ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="9b66c-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="9b66c-118">será retornado.</span><span class="sxs-lookup"><span data-stu-id="9b66c-118">error is returned.</span></span> <span data-ttu-id="9b66c-119">O ângulo resultante está no intervalo-PI/2 < = *Angle* _LT_ = pi/2 radianos (-90 < = *angle* < = 90 graus).</span><span class="sxs-lookup"><span data-stu-id="9b66c-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="9b66c-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9b66c-120">Example</span></span>

<span data-ttu-id="9b66c-121">ASEN (1)</span><span class="sxs-lookup"><span data-stu-id="9b66c-121">ASIN(1)</span></span>
  
<span data-ttu-id="9b66c-122">Retorna 90 graus</span><span class="sxs-lookup"><span data-stu-id="9b66c-122">Returns 90 deg</span></span>
  

