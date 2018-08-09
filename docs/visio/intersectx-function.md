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
description: Retorna o x-coordenada (no sistema de coordenadas locais) do ponto de interseção de duas linhas.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772080"
---
# <a name="intersectx-function"></a><span data-ttu-id="30b5b-103">Função INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="30b5b-103">INTERSECTX Function</span></span>

<span data-ttu-id="30b5b-104">Retorna o *x* -coordenada (no sistema de coordenadas locais) do ponto de interseção de duas linhas.</span><span class="sxs-lookup"><span data-stu-id="30b5b-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="30b5b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30b5b-105">Syntax</span></span>

<span data-ttu-id="30b5b-106">INTERSECTX (* * *x1* * *, * * *y1* * *, * * *angle1* * *, * * *x2* * *, * * *y2* * *, * * *angle2* * *)</span><span class="sxs-lookup"><span data-stu-id="30b5b-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="30b5b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30b5b-107">Parameters</span></span>

|<span data-ttu-id="30b5b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="30b5b-108">**Name**</span></span>|<span data-ttu-id="30b5b-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="30b5b-109">**Required/Optional**</span></span>|<span data-ttu-id="30b5b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="30b5b-110">**Data Type**</span></span>|<span data-ttu-id="30b5b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30b5b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="30b5b-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="30b5b-112">_x1_</span></span> <br/> |<span data-ttu-id="30b5b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30b5b-113">Required</span></span>  <br/> |<span data-ttu-id="30b5b-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="30b5b-114">**Number**</span></span> <br/> |<span data-ttu-id="30b5b-115">_X_-coordenadas de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="30b5b-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="30b5b-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="30b5b-116">_y1_</span></span> <br/> |<span data-ttu-id="30b5b-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30b5b-117">Required</span></span>  <br/> |<span data-ttu-id="30b5b-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="30b5b-118">**Number**</span></span> <br/> |<span data-ttu-id="30b5b-119">_Y_-coordenadas de um ponto na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="30b5b-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="30b5b-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="30b5b-120">_angle1_</span></span> <br/> |<span data-ttu-id="30b5b-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30b5b-121">Required</span></span>  <br/> |<span data-ttu-id="30b5b-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="30b5b-122">**Number**</span></span> <br/> | <span data-ttu-id="30b5b-123">O valor da célula Angle da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="30b5b-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="30b5b-124">_X2_</span><span class="sxs-lookup"><span data-stu-id="30b5b-124">_x2_</span></span> <br/> |<span data-ttu-id="30b5b-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30b5b-125">Required</span></span>  <br/> |<span data-ttu-id="30b5b-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="30b5b-126">**Number**</span></span> <br/> |<span data-ttu-id="30b5b-127">_X_-coordenadas de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="30b5b-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="30b5b-128">_a2_</span><span class="sxs-lookup"><span data-stu-id="30b5b-128">_y2_</span></span> <br/> |<span data-ttu-id="30b5b-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30b5b-129">Required</span></span>  <br/> |<span data-ttu-id="30b5b-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="30b5b-130">**Number**</span></span> <br/> |<span data-ttu-id="30b5b-131">_Y_-coordenadas de um ponto na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="30b5b-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="30b5b-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="30b5b-132">_angle2_</span></span> <br/> |<span data-ttu-id="30b5b-133">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30b5b-133">Required</span></span>  <br/> |<span data-ttu-id="30b5b-134">**Número**</span><span class="sxs-lookup"><span data-stu-id="30b5b-134">**Number**</span></span> <br/> |<span data-ttu-id="30b5b-135">O valor da célula Angle da segunda linha.</span><span class="sxs-lookup"><span data-stu-id="30b5b-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="30b5b-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="30b5b-136">Return value</span></span>

<span data-ttu-id="30b5b-137">Number</span><span class="sxs-lookup"><span data-stu-id="30b5b-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30b5b-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="30b5b-138">Remarks</span></span>

<span data-ttu-id="30b5b-139">Cada linha é definida como um ponto (*x,y*) e um ângulo.</span><span class="sxs-lookup"><span data-stu-id="30b5b-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="30b5b-140">O Microsoft Visio utiliza essa função na célula PinX de uma forma colada a uma guia girada.</span><span class="sxs-lookup"><span data-stu-id="30b5b-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="30b5b-141">Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto.</span><span class="sxs-lookup"><span data-stu-id="30b5b-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="30b5b-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="30b5b-142">Example</span></span>

<span data-ttu-id="30b5b-143">INTERSECTX (VertGuide! PinX, VertGuide! PinY, VertGuide! Ângulo, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Ângulo)</span><span class="sxs-lookup"><span data-stu-id="30b5b-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="30b5b-144">Retorna o *x* -coordenadas do ponto de interseção de VertGuide e HorzGuide em unidades de página.</span><span class="sxs-lookup"><span data-stu-id="30b5b-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  
