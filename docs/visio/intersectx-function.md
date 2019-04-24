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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335305"
---
# <a name="intersectx-function"></a><span data-ttu-id="1e92c-103">Função INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="1e92c-103">INTERSECTX Function</span></span>

<span data-ttu-id="1e92c-104">Retorna a coordenada *x* (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção.</span><span class="sxs-lookup"><span data-stu-id="1e92c-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1e92c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e92c-105">Syntax</span></span>

<span data-ttu-id="1e92c-106">INTERSECTX (\* \* *X1* \* \*, \* \* *Y1* \* \*, \* \* *angle1* \* \*, \* \* *X2* \* \*, \* \* *Y2* \* \*, \* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1e92c-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e92c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e92c-107">Parameters</span></span>

|<span data-ttu-id="1e92c-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1e92c-108">**Name**</span></span>|<span data-ttu-id="1e92c-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="1e92c-109">**Required/Optional**</span></span>|<span data-ttu-id="1e92c-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1e92c-110">**Data Type**</span></span>|<span data-ttu-id="1e92c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1e92c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e92c-112">_X1_</span><span class="sxs-lookup"><span data-stu-id="1e92c-112">_x1_</span></span> <br/> |<span data-ttu-id="1e92c-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e92c-113">Required</span></span>  <br/> |<span data-ttu-id="1e92c-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e92c-114">**Number**</span></span> <br/> |<span data-ttu-id="1e92c-115">A coordenada _x_de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="1e92c-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="1e92c-116">_a1_</span><span class="sxs-lookup"><span data-stu-id="1e92c-116">_y1_</span></span> <br/> |<span data-ttu-id="1e92c-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e92c-117">Required</span></span>  <br/> |<span data-ttu-id="1e92c-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e92c-118">**Number**</span></span> <br/> |<span data-ttu-id="1e92c-119">A coordenada _y_de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="1e92c-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="1e92c-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="1e92c-120">_angle1_</span></span> <br/> |<span data-ttu-id="1e92c-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e92c-121">Required</span></span>  <br/> |<span data-ttu-id="1e92c-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e92c-122">**Number**</span></span> <br/> | <span data-ttu-id="1e92c-123">O valor da célula Angle da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="1e92c-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="1e92c-124">_X2_</span><span class="sxs-lookup"><span data-stu-id="1e92c-124">_x2_</span></span> <br/> |<span data-ttu-id="1e92c-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e92c-125">Required</span></span>  <br/> |<span data-ttu-id="1e92c-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e92c-126">**Number**</span></span> <br/> |<span data-ttu-id="1e92c-127">A coordenada _x_de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="1e92c-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="1e92c-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="1e92c-128">_y2_</span></span> <br/> |<span data-ttu-id="1e92c-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e92c-129">Required</span></span>  <br/> |<span data-ttu-id="1e92c-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e92c-130">**Number**</span></span> <br/> |<span data-ttu-id="1e92c-131">A coordenada _y_de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="1e92c-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="1e92c-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="1e92c-132">_angle2_</span></span> <br/> |<span data-ttu-id="1e92c-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e92c-133">Required</span></span>  <br/> |<span data-ttu-id="1e92c-134">**Número**</span><span class="sxs-lookup"><span data-stu-id="1e92c-134">**Number**</span></span> <br/> |<span data-ttu-id="1e92c-135">O valor da célula Angle da segunda linha.</span><span class="sxs-lookup"><span data-stu-id="1e92c-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1e92c-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1e92c-136">Return value</span></span>

<span data-ttu-id="1e92c-137">Número</span><span class="sxs-lookup"><span data-stu-id="1e92c-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e92c-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e92c-138">Remarks</span></span>

<span data-ttu-id="1e92c-139">Cada linha é definida como um ponto (*x,y*) e um ângulo.</span><span class="sxs-lookup"><span data-stu-id="1e92c-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="1e92c-140">O Microsoft Visio utiliza essa função na célula PinX de uma forma colada a uma guia girada.</span><span class="sxs-lookup"><span data-stu-id="1e92c-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="1e92c-141">Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto.</span><span class="sxs-lookup"><span data-stu-id="1e92c-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1e92c-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1e92c-142">Example</span></span>

<span data-ttu-id="1e92c-143">INTERSECTX (VertGuide! PinX, VertGuide! PinY, VertGuide! Ângulo, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Reto</span><span class="sxs-lookup"><span data-stu-id="1e92c-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="1e92c-144">Retorna a coordenada *x* do ponto de interseção de VertGuide e HorzGuide em unidades de página.</span><span class="sxs-lookup"><span data-stu-id="1e92c-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

