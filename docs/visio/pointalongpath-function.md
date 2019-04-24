---
title: Função POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348255"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="c9925-103">Função POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="c9925-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="c9925-104">Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.</span><span class="sxs-lookup"><span data-stu-id="c9925-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="c9925-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="c9925-105">Version Information</span></span>

<span data-ttu-id="c9925-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="c9925-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c9925-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9925-107">Syntax</span></span>

<span data-ttu-id="c9925-108">POINTALONGPATH (\* \* *seção* \* \*, \* \* *viagem* \* \* \* \* *[, deslocamento]* \* \* \* \* *[, segmento]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c9925-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c9925-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9925-109">Parameters</span></span>

|<span data-ttu-id="c9925-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c9925-110">**Name**</span></span>|<span data-ttu-id="c9925-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="c9925-111">**Required/Optional**</span></span>|<span data-ttu-id="c9925-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c9925-112">**Data Type**</span></span>|<span data-ttu-id="c9925-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c9925-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c9925-114">_section_</span><span class="sxs-lookup"><span data-stu-id="c9925-114">_section_</span></span> <br/> |<span data-ttu-id="c9925-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c9925-115">Required</span></span>  <br/> |<span data-ttu-id="c9925-116">**String**</span><span class="sxs-lookup"><span data-stu-id="c9925-116">**String**</span></span> <br/> |<span data-ttu-id="c9925-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="c9925-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="c9925-118">_transmiti_</span><span class="sxs-lookup"><span data-stu-id="c9925-118">_travel_</span></span> <br/> |<span data-ttu-id="c9925-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c9925-119">Required</span></span>  <br/> |<span data-ttu-id="c9925-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="c9925-120">**Double**</span></span> <br/> |<span data-ttu-id="c9925-121">O percentual do caminho percorrido, do ponto inicial ao ponto final, que identifica o ponto.</span><span class="sxs-lookup"><span data-stu-id="c9925-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="c9925-122">Deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="c9925-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="c9925-123">_partida_</span><span class="sxs-lookup"><span data-stu-id="c9925-123">_offset_</span></span> <br/> |<span data-ttu-id="c9925-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="c9925-124">Optional</span></span>  <br/> |<span data-ttu-id="c9925-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="c9925-125">**Double**</span></span> <br/> |<span data-ttu-id="c9925-126">A distância que esse ponto é deslocado do caminho.</span><span class="sxs-lookup"><span data-stu-id="c9925-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="c9925-127">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9925-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="c9925-128">_segmento_</span><span class="sxs-lookup"><span data-stu-id="c9925-128">_segment_</span></span> <br/> |<span data-ttu-id="c9925-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="c9925-129">Optional</span></span>  <br/> |<span data-ttu-id="c9925-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c9925-130">**Integer**</span></span> <br/> |<span data-ttu-id="c9925-131">O segmento baseado em 1 do caminho no qual as coordenadas deverão ser calculadas.</span><span class="sxs-lookup"><span data-stu-id="c9925-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c9925-132">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c9925-132">Return value</span></span>

 <span data-ttu-id="c9925-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="c9925-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9925-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9925-134">Remarks</span></span>

<span data-ttu-id="c9925-135">Se a _seção_ ou o _segmento_ não existir, o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="c9925-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="c9925-136">Valores de *deslocamento* positivos especificam pontos à esquerda da direção da viagem.</span><span class="sxs-lookup"><span data-stu-id="c9925-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="c9925-137">Valores de *deslocamento* negativos especificam pontos à direita da direção da viagem.</span><span class="sxs-lookup"><span data-stu-id="c9925-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="c9925-138">Um **Point** representa um par ordenado de coordenadas geométricas (*x,y*) como um único valor.</span><span class="sxs-lookup"><span data-stu-id="c9925-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

