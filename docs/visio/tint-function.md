---
title: Função TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica a cor aumentando a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro int.
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773157"
---
# <a name="tint-function"></a><span data-ttu-id="e4336-103">Função TINT</span><span class="sxs-lookup"><span data-stu-id="e4336-103">TINT Function</span></span>

<span data-ttu-id="e4336-104">Modifica a cor aumentando a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="e4336-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e4336-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4336-105">Syntax</span></span>

<span data-ttu-id="e4336-106">TONALIDADE (* * *cor* * *, * * *int* * *)</span><span class="sxs-lookup"><span data-stu-id="e4336-106">TINT(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4336-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4336-107">Parameters</span></span>

|<span data-ttu-id="e4336-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e4336-108">**Name**</span></span>|<span data-ttu-id="e4336-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e4336-109">**Required/Optional**</span></span>|<span data-ttu-id="e4336-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e4336-110">**Data Type**</span></span>|<span data-ttu-id="e4336-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e4336-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4336-112">_color_</span><span class="sxs-lookup"><span data-stu-id="e4336-112">_color_</span></span> <br/> |<span data-ttu-id="e4336-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e4336-113">Required</span></span>  <br/> |<span data-ttu-id="e4336-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="e4336-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e4336-115">O índice de cores do Microsoft Visio ou o valor RGB da cor.</span><span class="sxs-lookup"><span data-stu-id="e4336-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="e4336-116">_int_</span><span class="sxs-lookup"><span data-stu-id="e4336-116">_int_</span></span> <br/> |<span data-ttu-id="e4336-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e4336-117">Required</span></span>  <br/> |<span data-ttu-id="e4336-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e4336-118">**Integer**</span></span> <br/> |<span data-ttu-id="e4336-p101">O valor pelo qual a luminosidade da cor será aumentada. Pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="e4336-p101">The amount by which to increase the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e4336-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e4336-121">Return value</span></span>

 <span data-ttu-id="e4336-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="e4336-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4336-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4336-123">Remarks</span></span>

<span data-ttu-id="e4336-124">Os limites superiores e inferiores de luminosidade são 0 e 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e4336-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="e4336-125">Não há nenhum limite do tamanho do inteiro, que você pode passar para o parâmetro _int_ , mas luminosidade nunca excede esses limites.</span><span class="sxs-lookup"><span data-stu-id="e4336-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

