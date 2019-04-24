---
title: Função BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mistura duas cores na proporção especificada pelo parâmetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303294"
---
# <a name="blend-function"></a><span data-ttu-id="0b541-103">Função BLEND</span><span class="sxs-lookup"><span data-stu-id="0b541-103">BLEND Function</span></span>

<span data-ttu-id="0b541-104">Mistura duas cores na proporção especificada pelo parâmetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="0b541-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0b541-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b541-105">Syntax</span></span>

<span data-ttu-id="0b541-106">BLEND (\* \* *color1* \* \*, \* \* *color2* \* \*, \* \* *float [0, 1]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0b541-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0b541-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b541-107">Parameters</span></span>

|<span data-ttu-id="0b541-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0b541-108">**Name**</span></span>|<span data-ttu-id="0b541-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="0b541-109">**Required/Optional**</span></span>|<span data-ttu-id="0b541-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="0b541-110">**Data Type**</span></span>|<span data-ttu-id="0b541-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0b541-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0b541-112">_Color1_</span><span class="sxs-lookup"><span data-stu-id="0b541-112">_color1_</span></span> <br/> |<span data-ttu-id="0b541-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0b541-113">Required</span></span>  <br/> |<span data-ttu-id="0b541-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="0b541-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0b541-115">O índice de cores do Visio ou o valor RGB da primeira cor.</span><span class="sxs-lookup"><span data-stu-id="0b541-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="0b541-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="0b541-116">_color2_</span></span> <br/> |<span data-ttu-id="0b541-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0b541-117">Required</span></span>  <br/> |<span data-ttu-id="0b541-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="0b541-118">**Numeric**</span></span> <br/> |<span data-ttu-id="0b541-119">O índice de cores do Visio ou o valor RGB da segunda cor.</span><span class="sxs-lookup"><span data-stu-id="0b541-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="0b541-120">_float [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="0b541-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="0b541-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0b541-121">Required</span></span>  <br/> |<span data-ttu-id="0b541-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="0b541-122">**Float**</span></span> <br/> |<span data-ttu-id="0b541-123">A proporção na qual misturar _color2_ e _color1_, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0b541-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="0b541-124">Um número real de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="0b541-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0b541-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0b541-125">Return value</span></span>

 <span data-ttu-id="0b541-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="0b541-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b541-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b541-127">Remarks</span></span>

<span data-ttu-id="0b541-128">A cor retornada é determinada pelas proporções relativas para misturar _color2_ e _color1_, respectivamente, conforme especificado pelo parâmetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="0b541-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="0b541-129">Por exemplo, se _float_ for 0,25, a cor retornada será composta 75% de _color1_ e 25% de _color2_.</span><span class="sxs-lookup"><span data-stu-id="0b541-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="0b541-130">Outra maneira de pensar nisso é que o valor _float_ corresponde ao ponto ao longo do espectro de cores de _color1_ para _color2_.</span><span class="sxs-lookup"><span data-stu-id="0b541-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="0b541-131">Por esse motivo, números menores (mais próximos de __ zero) para flutuação de misturas são mais próximos de _color1_, enquanto números maiores (mais próximos de 1) produzem misturas mais próximas de _color2_.</span><span class="sxs-lookup"><span data-stu-id="0b541-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

