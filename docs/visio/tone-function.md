---
title: Função TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica a cor diminuindo sua saturação pela quantidade especificada no parâmetro int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434372"
---
# <a name="tone-function"></a><span data-ttu-id="57cc6-103">Função TONE</span><span class="sxs-lookup"><span data-stu-id="57cc6-103">TONE Function</span></span>

<span data-ttu-id="57cc6-104">Modifica a cor diminuindo sua saturação pela quantidade especificada no _parâmetro int._</span><span class="sxs-lookup"><span data-stu-id="57cc6-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="57cc6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57cc6-105">Syntax</span></span>

<span data-ttu-id="57cc6-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="57cc6-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="57cc6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57cc6-107">Parameters</span></span>

|<span data-ttu-id="57cc6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="57cc6-108">**Name**</span></span>|<span data-ttu-id="57cc6-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="57cc6-109">**Required/Optional**</span></span>|<span data-ttu-id="57cc6-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="57cc6-110">**Data Type**</span></span>|<span data-ttu-id="57cc6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="57cc6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="57cc6-112">_color_</span><span class="sxs-lookup"><span data-stu-id="57cc6-112">_color_</span></span> <br/> |<span data-ttu-id="57cc6-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="57cc6-113">Required</span></span>  <br/> |<span data-ttu-id="57cc6-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="57cc6-114">**Numeric**</span></span> <br/> |<span data-ttu-id="57cc6-115">O índice de cores do Microsoft Visio ou o valor RGB da cor.</span><span class="sxs-lookup"><span data-stu-id="57cc6-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="57cc6-116">_int_</span><span class="sxs-lookup"><span data-stu-id="57cc6-116">_int_</span></span> <br/> |<span data-ttu-id="57cc6-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="57cc6-117">Required</span></span>  <br/> |<span data-ttu-id="57cc6-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="57cc6-118">**Integer**</span></span> <br/> |<span data-ttu-id="57cc6-119">O valor pelo qual a saturação da cor será reduzida.</span><span class="sxs-lookup"><span data-stu-id="57cc6-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="57cc6-120">Pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="57cc6-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="57cc6-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="57cc6-121">Return value</span></span>

 <span data-ttu-id="57cc6-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="57cc6-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57cc6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="57cc6-123">Remarks</span></span>

<span data-ttu-id="57cc6-124">Os limites superior e inferior de saturação são, respectivamente, 0 e 240.</span><span class="sxs-lookup"><span data-stu-id="57cc6-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="57cc6-125">Não há limite para o tamanho do inteiro que você pode passar para o parâmetro  _int,_ mas a saturação nunca excede esses limites.</span><span class="sxs-lookup"><span data-stu-id="57cc6-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

