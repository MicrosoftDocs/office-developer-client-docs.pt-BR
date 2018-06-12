---
title: Função ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Retorna o ângulo da tangente para o caminho em um determinado ponto.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771289"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="0d9f4-103">Função ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="0d9f4-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="0d9f4-104">Retorna o ângulo da tangente para o caminho em um determinado ponto.</span><span class="sxs-lookup"><span data-stu-id="0d9f4-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="0d9f4-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="0d9f4-105">Version Information</span></span>

<span data-ttu-id="0d9f4-106">Versão adicionada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="0d9f4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0d9f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d9f4-107">Syntax</span></span>

<span data-ttu-id="0d9f4-108">ANGLEALONGPATH (* * *seção* * *, * * *de viagem* * * * * *[, segmento]* * *)</span><span class="sxs-lookup"><span data-stu-id="0d9f4-108">ANGLEALONGPATH(** *section* **, ** *travel* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0d9f4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d9f4-109">Parameters</span></span>

|<span data-ttu-id="0d9f4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-110">**Name**</span></span>|<span data-ttu-id="0d9f4-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-111">**Required/Optional**</span></span>|<span data-ttu-id="0d9f4-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-112">**Data Type**</span></span>|<span data-ttu-id="0d9f4-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0d9f4-114">_section_</span><span class="sxs-lookup"><span data-stu-id="0d9f4-114">_section_</span></span> <br/> |<span data-ttu-id="0d9f4-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0d9f4-115">Required</span></span>  <br/> |<span data-ttu-id="0d9f4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-116">**String**</span></span> <br/> |<span data-ttu-id="0d9f4-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="0d9f4-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="0d9f4-118">_viagem_</span><span class="sxs-lookup"><span data-stu-id="0d9f4-118">_travel_</span></span> <br/> |<span data-ttu-id="0d9f4-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0d9f4-119">Required</span></span>  <br/> |<span data-ttu-id="0d9f4-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-120">**Double**</span></span> <br/> |<span data-ttu-id="0d9f4-p101">O percentual no caminho do ponto inicial ao ponto final. Deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="0d9f4-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="0d9f4-123">_segmento_</span><span class="sxs-lookup"><span data-stu-id="0d9f4-123">_segment_</span></span> <br/> |<span data-ttu-id="0d9f4-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="0d9f4-124">Optional</span></span>  <br/> |<span data-ttu-id="0d9f4-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-125">**Integer**</span></span> <br/> |<span data-ttu-id="0d9f4-126">O segmento baseado em 1 do caminho no qual o ângulo da tangente deverá ser calculado.</span><span class="sxs-lookup"><span data-stu-id="0d9f4-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0d9f4-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0d9f4-127">Return value</span></span>

 <span data-ttu-id="0d9f4-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="0d9f4-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d9f4-129">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0d9f4-129">Remarks</span></span>

<span data-ttu-id="0d9f4-130">Se você incluir um valor _segment_ , ANGLEALONGPATH retornará o valor para esse segmento apenas.</span><span class="sxs-lookup"><span data-stu-id="0d9f4-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="0d9f4-131">Se você incluir um valor _segment_ , ANGLEALONGPATH determinará o ponto da tangente usando _viajam_ para calcular o percentual em _segment_.</span><span class="sxs-lookup"><span data-stu-id="0d9f4-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="0d9f4-132">Se não existir _section_ nem _segment_ , o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="0d9f4-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

