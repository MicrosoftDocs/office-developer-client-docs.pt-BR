---
title: Função TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica a cor diminuindo sua saturação pelo valor especificado no parâmetro int.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773167"
---
# <a name="tone-function"></a><span data-ttu-id="48f7e-103">Função TONE</span><span class="sxs-lookup"><span data-stu-id="48f7e-103">TONE Function</span></span>

<span data-ttu-id="48f7e-104">Modifica a cor diminuindo sua saturação pelo valor especificado no parâmetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="48f7e-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="48f7e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48f7e-105">Syntax</span></span>

<span data-ttu-id="48f7e-106">TOM (* * *cor* * *, * * *int* * *)</span><span class="sxs-lookup"><span data-stu-id="48f7e-106">TONE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="48f7e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48f7e-107">Parameters</span></span>

|<span data-ttu-id="48f7e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="48f7e-108">**Name**</span></span>|<span data-ttu-id="48f7e-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="48f7e-109">**Required/Optional**</span></span>|<span data-ttu-id="48f7e-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="48f7e-110">**Data Type**</span></span>|<span data-ttu-id="48f7e-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48f7e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="48f7e-112">_color_</span><span class="sxs-lookup"><span data-stu-id="48f7e-112">_color_</span></span> <br/> |<span data-ttu-id="48f7e-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="48f7e-113">Required</span></span>  <br/> |<span data-ttu-id="48f7e-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="48f7e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="48f7e-115">O índice de cores do Microsoft Visio ou o valor RGB da cor.</span><span class="sxs-lookup"><span data-stu-id="48f7e-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="48f7e-116">_int_</span><span class="sxs-lookup"><span data-stu-id="48f7e-116">_int_</span></span> <br/> |<span data-ttu-id="48f7e-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="48f7e-117">Required</span></span>  <br/> |<span data-ttu-id="48f7e-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="48f7e-118">**Integer**</span></span> <br/> |<span data-ttu-id="48f7e-p101">O valor pelo qual a saturação da cor será reduzida. Pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="48f7e-p101">The amount by which to decrease the saturation of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="48f7e-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="48f7e-121">Return value</span></span>

 <span data-ttu-id="48f7e-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="48f7e-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48f7e-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="48f7e-123">Remarks</span></span>

<span data-ttu-id="48f7e-124">Os limites superiores e inferiores de saturação são 0 e 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="48f7e-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="48f7e-125">Não há nenhum limite do tamanho do inteiro, que você pode passar para o parâmetro _int_ , mas saturação nunca excede esses limites.</span><span class="sxs-lookup"><span data-stu-id="48f7e-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

