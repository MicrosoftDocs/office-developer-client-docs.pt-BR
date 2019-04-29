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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432818"
---
# <a name="asin-function"></a><span data-ttu-id="b71fd-103">Função ASIN</span><span class="sxs-lookup"><span data-stu-id="b71fd-103">ASIN Function</span></span>

<span data-ttu-id="b71fd-104">Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é *núm* .</span><span class="sxs-lookup"><span data-stu-id="b71fd-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b71fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b71fd-105">Syntax</span></span>

<span data-ttu-id="b71fd-106">Asen (\* \* *número* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b71fd-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b71fd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b71fd-107">Parameters</span></span>

|<span data-ttu-id="b71fd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b71fd-108">**Name**</span></span>|<span data-ttu-id="b71fd-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="b71fd-109">**Required/Optional**</span></span>|<span data-ttu-id="b71fd-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="b71fd-110">**Data Type**</span></span>|<span data-ttu-id="b71fd-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b71fd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b71fd-112">_number_</span><span class="sxs-lookup"><span data-stu-id="b71fd-112">_number_</span></span> <br/> |<span data-ttu-id="b71fd-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b71fd-113">Required</span></span>  <br/> |<span data-ttu-id="b71fd-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="b71fd-114">**Numeric**</span></span> <br/> |<span data-ttu-id="b71fd-115">O seno do ângulo.</span><span class="sxs-lookup"><span data-stu-id="b71fd-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b71fd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b71fd-116">Remarks</span></span>

<span data-ttu-id="b71fd-117">O valor de entrada deve estar no intervalo-1 < = *Number* < = 1, ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="b71fd-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="b71fd-118">será retornado.</span><span class="sxs-lookup"><span data-stu-id="b71fd-118">error is returned.</span></span> <span data-ttu-id="b71fd-119">O ângulo resultante está no intervalo-PI/2 < = *Angle* _LT_ = pi/2 radianos (-90 < = *angle* < = 90 graus).</span><span class="sxs-lookup"><span data-stu-id="b71fd-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="b71fd-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b71fd-120">Example</span></span>

<span data-ttu-id="b71fd-121">ASEN (1)</span><span class="sxs-lookup"><span data-stu-id="b71fd-121">ASIN(1)</span></span>
  
<span data-ttu-id="b71fd-122">Retorna 90 graus</span><span class="sxs-lookup"><span data-stu-id="b71fd-122">Returns 90 deg</span></span>
  

