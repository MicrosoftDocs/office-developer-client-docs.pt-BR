---
title: Função TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica a cor aumentando sua luminosidade pela quantidade (positiva ou negativa) especificada no parâmetro int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406574"
---
# <a name="tint-function"></a><span data-ttu-id="0a103-103">Função TINT</span><span class="sxs-lookup"><span data-stu-id="0a103-103">TINT Function</span></span>

<span data-ttu-id="0a103-104">Modifica a cor aumentando sua luminosidade pela quantidade (positiva ou negativa) especificada no _parâmetro int._</span><span class="sxs-lookup"><span data-stu-id="0a103-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0a103-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a103-105">Syntax</span></span>

<span data-ttu-id="0a103-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="0a103-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a103-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a103-107">Parameters</span></span>

|<span data-ttu-id="0a103-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a103-108">**Name**</span></span>|<span data-ttu-id="0a103-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="0a103-109">**Required/Optional**</span></span>|<span data-ttu-id="0a103-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="0a103-110">**Data Type**</span></span>|<span data-ttu-id="0a103-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0a103-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a103-112">_color_</span><span class="sxs-lookup"><span data-stu-id="0a103-112">_color_</span></span> <br/> |<span data-ttu-id="0a103-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a103-113">Required</span></span>  <br/> |<span data-ttu-id="0a103-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="0a103-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0a103-115">O índice de cores do Microsoft Visio ou o valor RGB da cor.</span><span class="sxs-lookup"><span data-stu-id="0a103-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="0a103-116">_int_</span><span class="sxs-lookup"><span data-stu-id="0a103-116">_int_</span></span> <br/> |<span data-ttu-id="0a103-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a103-117">Required</span></span>  <br/> |<span data-ttu-id="0a103-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a103-118">**Integer**</span></span> <br/> |<span data-ttu-id="0a103-119">O valor pelo qual a luminosidade da cor será aumentada.</span><span class="sxs-lookup"><span data-stu-id="0a103-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="0a103-120">Pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="0a103-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0a103-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0a103-121">Return value</span></span>

 <span data-ttu-id="0a103-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="0a103-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a103-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a103-123">Remarks</span></span>

<span data-ttu-id="0a103-124">Os limites superior e inferior de luminosidade são, respectivamente, 0 e 240.</span><span class="sxs-lookup"><span data-stu-id="0a103-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="0a103-125">Não há limite para o tamanho do inteiro que você pode passar para o parâmetro  _int,_ mas a luminosidade nunca excede esses limites.</span><span class="sxs-lookup"><span data-stu-id="0a103-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

