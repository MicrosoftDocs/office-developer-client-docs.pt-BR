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
description: Retorna um ângulo transformado no sistema de coordenadas local da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino.
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433567"
---
# <a name="angletoloc-function"></a><span data-ttu-id="04753-104">Função ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="04753-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="04753-105">Retorna um ângulo transformado no sistema de coordenadas local da forma de destino.</span><span class="sxs-lookup"><span data-stu-id="04753-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="04753-106">Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino.</span><span class="sxs-lookup"><span data-stu-id="04753-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="04753-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04753-107">Syntax</span></span>

<span data-ttu-id="04753-108">ANGLETOLOC (\* \* *srcAngle* \* \*, \* \* *srcRef* \* \*, \* \* *dstRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="04753-108">ANGLETOLOC(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="04753-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04753-109">Parameters</span></span>

|<span data-ttu-id="04753-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="04753-110">**Name**</span></span>|<span data-ttu-id="04753-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="04753-111">**Required/Optional**</span></span>|<span data-ttu-id="04753-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="04753-112">**Data Type**</span></span>|<span data-ttu-id="04753-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="04753-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="04753-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="04753-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="04753-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="04753-115">Required</span></span>  <br/> |<span data-ttu-id="04753-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="04753-116">**Numeric**</span></span> <br/> |<span data-ttu-id="04753-117">Um ângulo no sistema de coordenadas de origem.</span><span class="sxs-lookup"><span data-stu-id="04753-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="04753-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="04753-118">_srcRef_</span></span> <br/> |<span data-ttu-id="04753-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="04753-119">Required</span></span>  <br/> |<span data-ttu-id="04753-120">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04753-120">**String**</span></span> <br/> | <span data-ttu-id="04753-121">Uma referência a uma célula no objeto de origem, como uma forma, um grupo, uma página, entre outros.</span><span class="sxs-lookup"><span data-stu-id="04753-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="04753-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="04753-122">_dstRef_</span></span> <br/> |<span data-ttu-id="04753-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="04753-123">Required</span></span>  <br/> |<span data-ttu-id="04753-124">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04753-124">**String**</span></span> <br/> |<span data-ttu-id="04753-125">Uma referência a uma célula no objeto de destino, como uma forma, um grupo, uma página, entre outros.</span><span class="sxs-lookup"><span data-stu-id="04753-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04753-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="04753-126">Remarks</span></span>

<span data-ttu-id="04753-127">Utilize a função ANGLETOLOC para definir células de ângulo locais em uma forma de um ângulo a partir de um outro espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="04753-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="04753-p103">Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.</span><span class="sxs-lookup"><span data-stu-id="04753-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="04753-130">As coordenadas de origem e de destino devem estar na mesma página.</span><span class="sxs-lookup"><span data-stu-id="04753-130">The source and destination coordinates must be on the same page.</span></span>
  

