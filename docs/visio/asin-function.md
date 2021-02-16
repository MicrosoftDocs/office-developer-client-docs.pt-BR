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
description: Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é número .
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293503"
---
# <a name="asin-function"></a><span data-ttu-id="82c2b-103">Função ASIN</span><span class="sxs-lookup"><span data-stu-id="82c2b-103">ASIN Function</span></span>

<span data-ttu-id="82c2b-104">Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é  *número*  .</span><span class="sxs-lookup"><span data-stu-id="82c2b-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="82c2b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82c2b-105">Syntax</span></span>

<span data-ttu-id="82c2b-106">ASIN(***number*** )</span><span class="sxs-lookup"><span data-stu-id="82c2b-106">ASIN(***number*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="82c2b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82c2b-107">Parameters</span></span>

|<span data-ttu-id="82c2b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="82c2b-108">**Name**</span></span>|<span data-ttu-id="82c2b-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="82c2b-109">**Required/Optional**</span></span>|<span data-ttu-id="82c2b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="82c2b-110">**Data Type**</span></span>|<span data-ttu-id="82c2b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="82c2b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="82c2b-112">_number_</span><span class="sxs-lookup"><span data-stu-id="82c2b-112">_number_</span></span> <br/> |<span data-ttu-id="82c2b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82c2b-113">Required</span></span>  <br/> |<span data-ttu-id="82c2b-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="82c2b-114">**Numeric**</span></span> <br/> |<span data-ttu-id="82c2b-115">O seno do ângulo.</span><span class="sxs-lookup"><span data-stu-id="82c2b-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82c2b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="82c2b-116">Remarks</span></span>

<span data-ttu-id="82c2b-117">O valor de entrada deve estar no intervalo -1 <=  *número*  <= 1 ou um #NUM!</span><span class="sxs-lookup"><span data-stu-id="82c2b-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="82c2b-118">será retornado.</span><span class="sxs-lookup"><span data-stu-id="82c2b-118">error is returned.</span></span> <span data-ttu-id="82c2b-119">O ângulo resultante está no intervalo -PI/2 < *=*  ângulo <= PI/2 radianos (-90 < *=*  ângulo <= 90 graus).</span><span class="sxs-lookup"><span data-stu-id="82c2b-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="82c2b-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="82c2b-120">Example</span></span>

<span data-ttu-id="82c2b-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="82c2b-121">ASIN(1)</span></span>
  
<span data-ttu-id="82c2b-122">Retorna 90 graus</span><span class="sxs-lookup"><span data-stu-id="82c2b-122">Returns 90 deg</span></span>
  

