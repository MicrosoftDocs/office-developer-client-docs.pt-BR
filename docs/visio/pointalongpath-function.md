---
title: Função POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772513"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="2712b-103">Função POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="2712b-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="2712b-104">Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.</span><span class="sxs-lookup"><span data-stu-id="2712b-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="2712b-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="2712b-105">Version Information</span></span>

<span data-ttu-id="2712b-106">Versão adicionada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="2712b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2712b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2712b-107">Syntax</span></span>

<span data-ttu-id="2712b-108">POINTALONGPATH (* * *seção* * *, * * *de viagem* * * * * *[, deslocamento]* * * * * *[, segmento]* * *)</span><span class="sxs-lookup"><span data-stu-id="2712b-108">POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2712b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2712b-109">Parameters</span></span>

|<span data-ttu-id="2712b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2712b-110">**Name**</span></span>|<span data-ttu-id="2712b-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2712b-111">**Required/Optional**</span></span>|<span data-ttu-id="2712b-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2712b-112">**Data Type**</span></span>|<span data-ttu-id="2712b-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2712b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2712b-114">_section_</span><span class="sxs-lookup"><span data-stu-id="2712b-114">_section_</span></span> <br/> |<span data-ttu-id="2712b-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2712b-115">Required</span></span>  <br/> |<span data-ttu-id="2712b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="2712b-116">**String**</span></span> <br/> |<span data-ttu-id="2712b-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="2712b-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="2712b-118">_viagem_</span><span class="sxs-lookup"><span data-stu-id="2712b-118">_travel_</span></span> <br/> |<span data-ttu-id="2712b-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2712b-119">Required</span></span>  <br/> |<span data-ttu-id="2712b-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="2712b-120">**Double**</span></span> <br/> |<span data-ttu-id="2712b-p101">O percentual do caminho percorrido, do ponto inicial ao ponto final, que identifica o ponto. Deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="2712b-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="2712b-123">_deslocamento_</span><span class="sxs-lookup"><span data-stu-id="2712b-123">_offset_</span></span> <br/> |<span data-ttu-id="2712b-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="2712b-124">Optional</span></span>  <br/> |<span data-ttu-id="2712b-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="2712b-125">**Double**</span></span> <br/> |<span data-ttu-id="2712b-p102">A distância que esse ponto é deslocado do caminho. Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2712b-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="2712b-128">_segmento_</span><span class="sxs-lookup"><span data-stu-id="2712b-128">_segment_</span></span> <br/> |<span data-ttu-id="2712b-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="2712b-129">Optional</span></span>  <br/> |<span data-ttu-id="2712b-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="2712b-130">**Integer**</span></span> <br/> |<span data-ttu-id="2712b-131">O segmento baseado em 1 do caminho no qual as coordenadas deverão ser calculadas.</span><span class="sxs-lookup"><span data-stu-id="2712b-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2712b-132">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2712b-132">Return value</span></span>

 <span data-ttu-id="2712b-133">**Ponto**</span><span class="sxs-lookup"><span data-stu-id="2712b-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2712b-134">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2712b-134">Remarks</span></span>

<span data-ttu-id="2712b-135">Se não existir _section_ nem _segment_ , o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="2712b-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="2712b-136">Valores de *deslocamento* de positivos especificam pontos à esquerda da direção da viagem.</span><span class="sxs-lookup"><span data-stu-id="2712b-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="2712b-137">Valores de *deslocamento* de negativos especificam pontos à direita da direção da viagem.</span><span class="sxs-lookup"><span data-stu-id="2712b-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="2712b-138">Um **Point** representa um par ordenado de coordenadas geométricas (*x, y*) como um valor único.</span><span class="sxs-lookup"><span data-stu-id="2712b-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

