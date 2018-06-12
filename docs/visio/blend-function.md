---
title: Função BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combina duas cores na proporção especificada pelo parâmetro float.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771391"
---
# <a name="blend-function"></a><span data-ttu-id="e85d8-103">Função BLEND</span><span class="sxs-lookup"><span data-stu-id="e85d8-103">BLEND Function</span></span>

<span data-ttu-id="e85d8-104">Combina duas cores na proporção especificada pelo parâmetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="e85d8-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e85d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e85d8-105">Syntax</span></span>

<span data-ttu-id="e85d8-106">MISTURA (* * *color1* * *, * * *color2* * *, * * *float [0,1]* * *)</span><span class="sxs-lookup"><span data-stu-id="e85d8-106">BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e85d8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e85d8-107">Parameters</span></span>

|<span data-ttu-id="e85d8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e85d8-108">**Name**</span></span>|<span data-ttu-id="e85d8-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e85d8-109">**Required/Optional**</span></span>|<span data-ttu-id="e85d8-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e85d8-110">**Data Type**</span></span>|<span data-ttu-id="e85d8-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e85d8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e85d8-112">_Color1_</span><span class="sxs-lookup"><span data-stu-id="e85d8-112">_color1_</span></span> <br/> |<span data-ttu-id="e85d8-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e85d8-113">Required</span></span>  <br/> |<span data-ttu-id="e85d8-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="e85d8-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e85d8-115">O índice de cores do Visio ou o valor RGB da primeira cor.</span><span class="sxs-lookup"><span data-stu-id="e85d8-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="e85d8-116">_Color2_</span><span class="sxs-lookup"><span data-stu-id="e85d8-116">_color2_</span></span> <br/> |<span data-ttu-id="e85d8-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e85d8-117">Required</span></span>  <br/> |<span data-ttu-id="e85d8-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="e85d8-118">**Numeric**</span></span> <br/> |<span data-ttu-id="e85d8-119">O índice de cores do Visio ou o valor RGB da segunda cor.</span><span class="sxs-lookup"><span data-stu-id="e85d8-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="e85d8-120">_float [0,1]_</span><span class="sxs-lookup"><span data-stu-id="e85d8-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="e85d8-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e85d8-121">Required</span></span>  <br/> |<span data-ttu-id="e85d8-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="e85d8-122">**Float**</span></span> <br/> |<span data-ttu-id="e85d8-123">A proporção no qual mesclar _color2_ e _color1_, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e85d8-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="e85d8-124">Um número de real entre 0 e 1 inclusive.</span><span class="sxs-lookup"><span data-stu-id="e85d8-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e85d8-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e85d8-125">Return value</span></span>

 <span data-ttu-id="e85d8-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="e85d8-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e85d8-127">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e85d8-127">Remarks</span></span>

<span data-ttu-id="e85d8-128">A cor retornada é determinada pelas proporções relativas no qual mesclar _color2_ e _color1_, respectivamente, conforme especificado pelo parâmetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="e85d8-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="e85d8-129">Por exemplo, se _float_ for 0,25, a cor retornada é compostas 75% das _cor1_ e 25% dos _color2_.</span><span class="sxs-lookup"><span data-stu-id="e85d8-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="e85d8-130">Outra maneira de pensar sobre ele é que o valor de _float_ corresponde ao ponto ao longo do espectro de cores de _color1_ para _color2_.</span><span class="sxs-lookup"><span data-stu-id="e85d8-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="e85d8-131">Portanto, menor números (mais próximo do zero) para quase misturas de produzir _float_ para _color1_, enquanto os números maior (mais perto de 1) produzem misturas quase _color2_.</span><span class="sxs-lookup"><span data-stu-id="e85d8-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

