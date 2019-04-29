---
title: Função INTERSECTX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Retorna a coordenada x (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418271"
---
# <a name="intersectx-function"></a><span data-ttu-id="9f38d-103">Função INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="9f38d-103">INTERSECTX Function</span></span>

<span data-ttu-id="9f38d-104">Retorna a coordenada *x* (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção.</span><span class="sxs-lookup"><span data-stu-id="9f38d-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f38d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f38d-105">Syntax</span></span>

<span data-ttu-id="9f38d-106">INTERSECTX (\* \* *X1* \* \*, \* \* *Y1* \* \*, \* \* *angle1* \* \*, \* \* *X2* \* \*, \* \* *Y2* \* \*, \* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9f38d-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f38d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f38d-107">Parameters</span></span>

|<span data-ttu-id="9f38d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f38d-108">**Name**</span></span>|<span data-ttu-id="9f38d-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="9f38d-109">**Required/Optional**</span></span>|<span data-ttu-id="9f38d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9f38d-110">**Data Type**</span></span>|<span data-ttu-id="9f38d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9f38d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f38d-112">_X1_</span><span class="sxs-lookup"><span data-stu-id="9f38d-112">_x1_</span></span> <br/> |<span data-ttu-id="9f38d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9f38d-113">Required</span></span>  <br/> |<span data-ttu-id="9f38d-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="9f38d-114">**Number**</span></span> <br/> |<span data-ttu-id="9f38d-115">A coordenada _x_de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="9f38d-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="9f38d-116">_a1_</span><span class="sxs-lookup"><span data-stu-id="9f38d-116">_y1_</span></span> <br/> |<span data-ttu-id="9f38d-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9f38d-117">Required</span></span>  <br/> |<span data-ttu-id="9f38d-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="9f38d-118">**Number**</span></span> <br/> |<span data-ttu-id="9f38d-119">A coordenada _y_de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="9f38d-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="9f38d-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="9f38d-120">_angle1_</span></span> <br/> |<span data-ttu-id="9f38d-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9f38d-121">Required</span></span>  <br/> |<span data-ttu-id="9f38d-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="9f38d-122">**Number**</span></span> <br/> | <span data-ttu-id="9f38d-123">O valor da célula Angle da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="9f38d-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="9f38d-124">_X2_</span><span class="sxs-lookup"><span data-stu-id="9f38d-124">_x2_</span></span> <br/> |<span data-ttu-id="9f38d-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9f38d-125">Required</span></span>  <br/> |<span data-ttu-id="9f38d-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="9f38d-126">**Number**</span></span> <br/> |<span data-ttu-id="9f38d-127">A coordenada _x_de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="9f38d-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="9f38d-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="9f38d-128">_y2_</span></span> <br/> |<span data-ttu-id="9f38d-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9f38d-129">Required</span></span>  <br/> |<span data-ttu-id="9f38d-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="9f38d-130">**Number**</span></span> <br/> |<span data-ttu-id="9f38d-131">A coordenada _y_de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="9f38d-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="9f38d-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="9f38d-132">_angle2_</span></span> <br/> |<span data-ttu-id="9f38d-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9f38d-133">Required</span></span>  <br/> |<span data-ttu-id="9f38d-134">**Número**</span><span class="sxs-lookup"><span data-stu-id="9f38d-134">**Number**</span></span> <br/> |<span data-ttu-id="9f38d-135">O valor da célula Angle da segunda linha.</span><span class="sxs-lookup"><span data-stu-id="9f38d-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9f38d-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f38d-136">Return value</span></span>

<span data-ttu-id="9f38d-137">Número</span><span class="sxs-lookup"><span data-stu-id="9f38d-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f38d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f38d-138">Remarks</span></span>

<span data-ttu-id="9f38d-139">Cada linha é definida como um ponto (*x,y*) e um ângulo.</span><span class="sxs-lookup"><span data-stu-id="9f38d-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="9f38d-140">O Microsoft Visio utiliza essa função na célula PinX de uma forma colada a uma guia girada.</span><span class="sxs-lookup"><span data-stu-id="9f38d-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="9f38d-141">Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto.</span><span class="sxs-lookup"><span data-stu-id="9f38d-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9f38d-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9f38d-142">Example</span></span>

<span data-ttu-id="9f38d-143">INTERSECTX (VertGuide! PinX, VertGuide! PinY, VertGuide! Ângulo, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Reto</span><span class="sxs-lookup"><span data-stu-id="9f38d-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="9f38d-144">Retorna a coordenada *x* do ponto de interseção de VertGuide e HorzGuide em unidades de página.</span><span class="sxs-lookup"><span data-stu-id="9f38d-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

