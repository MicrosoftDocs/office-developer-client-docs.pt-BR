---
title: Função ANGLETOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Retorna um ângulo transformado no sistema de coordenadas pai da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas pai em uma forma de destino.
ms.openlocfilehash: 3a739c55d568dc548f8175b56f22e6ec4c28e4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771277"
---
# <a name="angletopar-function"></a><span data-ttu-id="e0b85-104">Função ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="e0b85-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="e0b85-p102">Retorna um ângulo transformado no sistema de coordenadas pai da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas pai em uma forma de destino.
    
</span><span class="sxs-lookup"><span data-stu-id="e0b85-p102">Returns a transformed angle in the destination shape's parent coordinate system. Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e0b85-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b85-107">Syntax</span></span>

<span data-ttu-id="e0b85-108">ANGLETOPAR (* * *srcAngle* * *, * * *srcRef* * *, * * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="e0b85-108">ANGLETOPAR(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e0b85-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b85-109">Parameters</span></span>

|<span data-ttu-id="e0b85-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e0b85-110">**Name**</span></span>|<span data-ttu-id="e0b85-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e0b85-111">**Required/Optional**</span></span>|<span data-ttu-id="e0b85-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e0b85-112">**Data Type**</span></span>|<span data-ttu-id="e0b85-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e0b85-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e0b85-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="e0b85-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="e0b85-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e0b85-115">Required</span></span>  <br/> |<span data-ttu-id="e0b85-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="e0b85-116">**Numeric**</span></span> <br/> |<span data-ttu-id="e0b85-117">Um ângulo no sistema de coordenadas de origem.</span><span class="sxs-lookup"><span data-stu-id="e0b85-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="e0b85-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="e0b85-118">_srcRef_</span></span> <br/> |<span data-ttu-id="e0b85-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e0b85-119">Required</span></span>  <br/> |<span data-ttu-id="e0b85-120">**String**</span><span class="sxs-lookup"><span data-stu-id="e0b85-120">**String**</span></span> <br/> | <span data-ttu-id="e0b85-121">Uma referência a uma célula no objeto de origem, como uma forma, um grupo, uma página, entre outros.</span><span class="sxs-lookup"><span data-stu-id="e0b85-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="e0b85-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="e0b85-122">_dstRef_</span></span> <br/> |<span data-ttu-id="e0b85-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e0b85-123">Required</span></span>  <br/> |<span data-ttu-id="e0b85-124">**String**</span><span class="sxs-lookup"><span data-stu-id="e0b85-124">**String**</span></span> <br/> |<span data-ttu-id="e0b85-125">Uma referência a uma célula no objeto de destino, como uma forma, um grupo, uma página, entre outros.</span><span class="sxs-lookup"><span data-stu-id="e0b85-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0b85-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0b85-126">Remarks</span></span>

<span data-ttu-id="e0b85-p103">Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.</span><span class="sxs-lookup"><span data-stu-id="e0b85-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="e0b85-129">As coordenadas de origem e de destino devem estar na mesma página.</span><span class="sxs-lookup"><span data-stu-id="e0b85-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="e0b85-130">Se o destino for uma página que não tem um pai, o resultado será expresso em coordenadas locais da página.</span><span class="sxs-lookup"><span data-stu-id="e0b85-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

