---
title: Função ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Retorna o ângulo da tangente para o caminho em um determinado ponto.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341416"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="54b8d-103">Função ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="54b8d-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="54b8d-104">Retorna o ângulo da tangente para o caminho em um determinado ponto.</span><span class="sxs-lookup"><span data-stu-id="54b8d-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="54b8d-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="54b8d-105">Version Information</span></span>

<span data-ttu-id="54b8d-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="54b8d-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="54b8d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54b8d-107">Syntax</span></span>

<span data-ttu-id="54b8d-108">ANGLEALONGPATH (\* \* *seção* \* \*, \* \* *viagem* \* \* \* \* *[, segmento]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="54b8d-108">ANGLEALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="54b8d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54b8d-109">Parameters</span></span>

|<span data-ttu-id="54b8d-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="54b8d-110">**Name**</span></span>|<span data-ttu-id="54b8d-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="54b8d-111">**Required/Optional**</span></span>|<span data-ttu-id="54b8d-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="54b8d-112">**Data Type**</span></span>|<span data-ttu-id="54b8d-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54b8d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="54b8d-114">_section_</span><span class="sxs-lookup"><span data-stu-id="54b8d-114">_section_</span></span> <br/> |<span data-ttu-id="54b8d-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="54b8d-115">Required</span></span>  <br/> |<span data-ttu-id="54b8d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="54b8d-116">**String**</span></span> <br/> |<span data-ttu-id="54b8d-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="54b8d-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="54b8d-118">_transmiti_</span><span class="sxs-lookup"><span data-stu-id="54b8d-118">_travel_</span></span> <br/> |<span data-ttu-id="54b8d-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="54b8d-119">Required</span></span>  <br/> |<span data-ttu-id="54b8d-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="54b8d-120">**Double**</span></span> <br/> |<span data-ttu-id="54b8d-121">O percentual no caminho do ponto inicial ao ponto final.</span><span class="sxs-lookup"><span data-stu-id="54b8d-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="54b8d-122">Deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="54b8d-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="54b8d-123">_segmento_</span><span class="sxs-lookup"><span data-stu-id="54b8d-123">_segment_</span></span> <br/> |<span data-ttu-id="54b8d-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="54b8d-124">Optional</span></span>  <br/> |<span data-ttu-id="54b8d-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="54b8d-125">**Integer**</span></span> <br/> |<span data-ttu-id="54b8d-126">O segmento baseado em 1 do caminho no qual o ângulo da tangente deverá ser calculado.</span><span class="sxs-lookup"><span data-stu-id="54b8d-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="54b8d-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="54b8d-127">Return value</span></span>

 <span data-ttu-id="54b8d-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="54b8d-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54b8d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="54b8d-129">Remarks</span></span>

<span data-ttu-id="54b8d-130">Se você incluir um valor de _segmento_ , ANGLEALONGPATH retornará o valor somente para esse segmento.</span><span class="sxs-lookup"><span data-stu-id="54b8d-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="54b8d-131">Se você incluir um valor de _segmento_ , ANGLEALONGPATH determina o ponto da tangente usando a _viagem_ para calcular a percertment ao longo do _segmento_.</span><span class="sxs-lookup"><span data-stu-id="54b8d-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="54b8d-132">Se qualquer _seção_ ou _segmento_ não existir, o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="54b8d-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

