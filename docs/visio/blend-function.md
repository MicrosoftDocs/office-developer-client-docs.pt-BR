---
title: Função BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combina duas cores na proporção especificada pelo parâmetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432783"
---
# <a name="blend-function"></a><span data-ttu-id="2ffd5-103">Função BLEND</span><span class="sxs-lookup"><span data-stu-id="2ffd5-103">BLEND Function</span></span>

<span data-ttu-id="2ffd5-104">Combina duas cores na proporção especificada pelo parâmetro _float._</span><span class="sxs-lookup"><span data-stu-id="2ffd5-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2ffd5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ffd5-105">Syntax</span></span>

<span data-ttu-id="2ffd5-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2ffd5-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2ffd5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ffd5-107">Parameters</span></span>

|<span data-ttu-id="2ffd5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-108">**Name**</span></span>|<span data-ttu-id="2ffd5-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-109">**Required/Optional**</span></span>|<span data-ttu-id="2ffd5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-110">**Data Type**</span></span>|<span data-ttu-id="2ffd5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2ffd5-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="2ffd5-112">_color1_</span></span> <br/> |<span data-ttu-id="2ffd5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2ffd5-113">Required</span></span>  <br/> |<span data-ttu-id="2ffd5-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-114">**Numeric**</span></span> <br/> |<span data-ttu-id="2ffd5-115">O índice de cores do Visio ou o valor RGB da primeira cor.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="2ffd5-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="2ffd5-116">_color2_</span></span> <br/> |<span data-ttu-id="2ffd5-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2ffd5-117">Required</span></span>  <br/> |<span data-ttu-id="2ffd5-118">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-118">**Numeric**</span></span> <br/> |<span data-ttu-id="2ffd5-119">O índice de cores do Visio ou o valor RGB da segunda cor.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="2ffd5-120">_float[0,1]_</span><span class="sxs-lookup"><span data-stu-id="2ffd5-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="2ffd5-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2ffd5-121">Required</span></span>  <br/> |<span data-ttu-id="2ffd5-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-122">**Float**</span></span> <br/> |<span data-ttu-id="2ffd5-123">A proporção na qual mesclar  _color2_ e  _color1,_ respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="2ffd5-124">Um número real de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2ffd5-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2ffd5-125">Return value</span></span>

 <span data-ttu-id="2ffd5-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="2ffd5-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ffd5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ffd5-127">Remarks</span></span>

<span data-ttu-id="2ffd5-128">A cor retornada é determinada pelas proporções relativas nas quais a _cor2_ e _color1_ são mescladas, respectivamente, conforme especificado pelo parâmetro _float._</span><span class="sxs-lookup"><span data-stu-id="2ffd5-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="2ffd5-129">Por exemplo, se  _float_ for 0,25, a cor retornada será composta por 75% da  _cor1_ e 25% da  _cor2_.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="2ffd5-130">Outra maneira de pensar sobre  isso é que o valor flutuante corresponde ao ponto ao longo do espectro de cores de _color1_ a _color2_.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="2ffd5-131">Portanto, números menores (mais próximos de zero) para  _float_ produzem combinações mais próximas da  _cor1,_ enquanto números maiores (mais próximos de 1) produzem combinações mais próximas  _da cor2_.</span><span class="sxs-lookup"><span data-stu-id="2ffd5-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

