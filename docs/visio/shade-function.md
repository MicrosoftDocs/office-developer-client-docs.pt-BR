---
title: Função SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica a cor reduzindo sua luminosidade pelo valor (positivo ou negativo) especificado no parâmetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326591"
---
# <a name="shade-function"></a><span data-ttu-id="654e6-103">Função SHADE</span><span class="sxs-lookup"><span data-stu-id="654e6-103">SHADE Function</span></span>

<span data-ttu-id="654e6-104">Modifica a cor reduzindo sua luminosidade pelo valor (positivo ou negativo) especificado no parâmetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="654e6-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="654e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="654e6-105">Syntax</span></span>

<span data-ttu-id="654e6-106">SOMBREAmento (\* \* *cor* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="654e6-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="654e6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="654e6-107">Parameters</span></span>

|<span data-ttu-id="654e6-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="654e6-108">**Name**</span></span>|<span data-ttu-id="654e6-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="654e6-109">**Required/Optional**</span></span>|<span data-ttu-id="654e6-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="654e6-110">**Data Type**</span></span>|<span data-ttu-id="654e6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="654e6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="654e6-112">_color_</span><span class="sxs-lookup"><span data-stu-id="654e6-112">_color_</span></span> <br/> |<span data-ttu-id="654e6-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="654e6-113">Required</span></span>  <br/> |<span data-ttu-id="654e6-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="654e6-114">**Numeric**</span></span> <br/> |<span data-ttu-id="654e6-115">O índice de cores do Microsoft Visio ou o valor RGB da cor.</span><span class="sxs-lookup"><span data-stu-id="654e6-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="654e6-116">_int_</span><span class="sxs-lookup"><span data-stu-id="654e6-116">_int_</span></span> <br/> |<span data-ttu-id="654e6-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="654e6-117">Required</span></span>  <br/> |<span data-ttu-id="654e6-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="654e6-118">**Integer**</span></span> <br/> |<span data-ttu-id="654e6-119">O valor pelo qual a luminosidade da cor será reduzida.</span><span class="sxs-lookup"><span data-stu-id="654e6-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="654e6-120">Pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="654e6-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="654e6-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="654e6-121">Return value</span></span>

 <span data-ttu-id="654e6-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="654e6-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="654e6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="654e6-123">Remarks</span></span>

<span data-ttu-id="654e6-124">Os limites superior e inferior de luminosidade são, respectivamente, 0 e 240.</span><span class="sxs-lookup"><span data-stu-id="654e6-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="654e6-125">Não há limite para o tamanho do inteiro que você pode passar para o parâmetro _int_ , mas a luminosidade nunca excede esses limites.</span><span class="sxs-lookup"><span data-stu-id="654e6-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Limites superior e inferior de luminosidade](media/image199_ZA10173627.gif)
  

