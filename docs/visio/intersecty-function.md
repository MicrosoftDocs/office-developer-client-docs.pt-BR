---
title: Função INTERSECTY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Retorna a coordenada y (no sistema de coordenadas local) do ponto onde duas linhas se cruzam.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426097"
---
# <a name="intersecty-function"></a><span data-ttu-id="aadf4-103">Função INTERSECTY</span><span class="sxs-lookup"><span data-stu-id="aadf4-103">INTERSECTY Function</span></span>

<span data-ttu-id="aadf4-104">Retorna a  *coordenada y*  (no sistema de coordenadas local) do ponto onde duas linhas se cruzam.</span><span class="sxs-lookup"><span data-stu-id="aadf4-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aadf4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aadf4-105">Syntax</span></span>

<span data-ttu-id="aadf4-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="aadf4-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aadf4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aadf4-107">Parameters</span></span>

|<span data-ttu-id="aadf4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="aadf4-108">**Name**</span></span>|<span data-ttu-id="aadf4-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="aadf4-109">**Required/Optional**</span></span>|<span data-ttu-id="aadf4-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="aadf4-110">**Data Type**</span></span>|<span data-ttu-id="aadf4-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aadf4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aadf4-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="aadf4-112">_x1_</span></span> <br/> |<span data-ttu-id="aadf4-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aadf4-113">Required</span></span>  <br/> |<span data-ttu-id="aadf4-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="aadf4-114">**Number**</span></span> <br/> |<span data-ttu-id="aadf4-115">A  _coordenada x_ de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="aadf4-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="aadf4-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="aadf4-116">_y1_</span></span> <br/> |<span data-ttu-id="aadf4-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aadf4-117">Required</span></span>  <br/> |<span data-ttu-id="aadf4-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="aadf4-118">**Number**</span></span> <br/> |<span data-ttu-id="aadf4-119">A  _coordenada y_ de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="aadf4-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="aadf4-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="aadf4-120">_angle1_</span></span> <br/> |<span data-ttu-id="aadf4-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aadf4-121">Required</span></span>  <br/> |<span data-ttu-id="aadf4-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="aadf4-122">**Number**</span></span> <br/> | <span data-ttu-id="aadf4-123">O valor da célula Angle da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="aadf4-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="aadf4-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="aadf4-124">_x2_</span></span> <br/> |<span data-ttu-id="aadf4-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aadf4-125">Required</span></span>  <br/> |<span data-ttu-id="aadf4-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="aadf4-126">**Number**</span></span> <br/> |<span data-ttu-id="aadf4-127">A  _coordenada x_ de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="aadf4-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="aadf4-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="aadf4-128">_y2_</span></span> <br/> |<span data-ttu-id="aadf4-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aadf4-129">Required</span></span>  <br/> |<span data-ttu-id="aadf4-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="aadf4-130">**Number**</span></span> <br/> |<span data-ttu-id="aadf4-131">A  _coordenada y_ de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="aadf4-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="aadf4-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="aadf4-132">_angle2_</span></span> <br/> |<span data-ttu-id="aadf4-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aadf4-133">Required</span></span>  <br/> |<span data-ttu-id="aadf4-134">**Número**</span><span class="sxs-lookup"><span data-stu-id="aadf4-134">**Number**</span></span> <br/> |<span data-ttu-id="aadf4-135">O valor da célula Angle da segunda linha.</span><span class="sxs-lookup"><span data-stu-id="aadf4-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aadf4-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aadf4-136">Return value</span></span>

<span data-ttu-id="aadf4-137">Número</span><span class="sxs-lookup"><span data-stu-id="aadf4-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aadf4-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="aadf4-138">Remarks</span></span>

<span data-ttu-id="aadf4-139">Cada linha é definida como um ponto (*x,y*) e um ângulo.</span><span class="sxs-lookup"><span data-stu-id="aadf4-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="aadf4-140">O Microsoft Visio utiliza essa função na célula PinY de uma forma colada a uma guia girada.</span><span class="sxs-lookup"><span data-stu-id="aadf4-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="aadf4-141">Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto.</span><span class="sxs-lookup"><span data-stu-id="aadf4-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aadf4-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="aadf4-142">Example</span></span>

<span data-ttu-id="aadf4-143">INTERSECTY(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Ângulo)</span><span class="sxs-lookup"><span data-stu-id="aadf4-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="aadf4-144">Retorna a  *coordenada y*  do ponto de interseção de VertGuide e HorzGuide em unidades de página.</span><span class="sxs-lookup"><span data-stu-id="aadf4-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

