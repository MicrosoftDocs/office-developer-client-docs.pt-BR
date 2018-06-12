---
title: Função ANGLETOLOC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Retorna um ângulo transformado no sistema de coordenadas locais da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino.
ms.openlocfilehash: 09ab0a4a55446dd74729f1da0bcf022d8376909b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771269"
---
# <a name="angletoloc-function"></a><span data-ttu-id="637d8-104">Função ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="637d8-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="637d8-105">Retorna um ângulo transformado no sistema de coordenadas locais da forma de destino.</span><span class="sxs-lookup"><span data-stu-id="637d8-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="637d8-106">Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino.</span><span class="sxs-lookup"><span data-stu-id="637d8-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="637d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="637d8-107">Syntax</span></span>

<span data-ttu-id="637d8-108">ANGLETOLOC (* * *srcAngle* * *, * * *srcRef* * *, * * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="637d8-108">ANGLETOLOC(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="637d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="637d8-109">Parameters</span></span>

|<span data-ttu-id="637d8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="637d8-110">**Name**</span></span>|<span data-ttu-id="637d8-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="637d8-111">**Required/Optional**</span></span>|<span data-ttu-id="637d8-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="637d8-112">**Data Type**</span></span>|<span data-ttu-id="637d8-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="637d8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="637d8-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="637d8-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="637d8-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="637d8-115">Required</span></span>  <br/> |<span data-ttu-id="637d8-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="637d8-116">**Numeric**</span></span> <br/> |<span data-ttu-id="637d8-117">Um ângulo no sistema de coordenadas de origem.</span><span class="sxs-lookup"><span data-stu-id="637d8-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="637d8-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="637d8-118">_srcRef_</span></span> <br/> |<span data-ttu-id="637d8-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="637d8-119">Required</span></span>  <br/> |<span data-ttu-id="637d8-120">**String**</span><span class="sxs-lookup"><span data-stu-id="637d8-120">**String**</span></span> <br/> | <span data-ttu-id="637d8-121">Uma referência a uma célula no objeto de origem, como uma forma, um grupo, uma página, entre outros.</span><span class="sxs-lookup"><span data-stu-id="637d8-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="637d8-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="637d8-122">_dstRef_</span></span> <br/> |<span data-ttu-id="637d8-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="637d8-123">Required</span></span>  <br/> |<span data-ttu-id="637d8-124">**String**</span><span class="sxs-lookup"><span data-stu-id="637d8-124">**String**</span></span> <br/> |<span data-ttu-id="637d8-125">Uma referência a uma célula no objeto de destino, como uma forma, um grupo, uma página, entre outros.</span><span class="sxs-lookup"><span data-stu-id="637d8-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="637d8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="637d8-126">Remarks</span></span>

<span data-ttu-id="637d8-127">Utilize a função ANGLETOLOC para definir células de ângulo locais em uma forma de um ângulo a partir de um outro espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="637d8-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="637d8-p103">Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.</span><span class="sxs-lookup"><span data-stu-id="637d8-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="637d8-130">As coordenadas de origem e de destino devem estar na mesma página.</span><span class="sxs-lookup"><span data-stu-id="637d8-130">The source and destination coordinates must be on the same page.</span></span>
  

