---
title: Função PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Retorna o tamanho do caminho definido na seção Geometry especificada.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772473"
---
# <a name="pathlength-function"></a><span data-ttu-id="e6eea-103">Função PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="e6eea-103">PATHLENGTH Function</span></span>

<span data-ttu-id="e6eea-104">Retorna o tamanho do caminho definido na seção Geometry especificada.</span><span class="sxs-lookup"><span data-stu-id="e6eea-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e6eea-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="e6eea-105">Version Information</span></span>

<span data-ttu-id="e6eea-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="e6eea-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e6eea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6eea-107">Syntax</span></span>

<span data-ttu-id="e6eea-108">PATHLENGTH (* * *seção* * * * * *[, segmento]* * *)</span><span class="sxs-lookup"><span data-stu-id="e6eea-108">PATHLENGTH(** *section* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e6eea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6eea-109">Parameters</span></span>

|<span data-ttu-id="e6eea-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e6eea-110">**Name**</span></span>|<span data-ttu-id="e6eea-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e6eea-111">**Required/Optional**</span></span>|<span data-ttu-id="e6eea-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e6eea-112">**Data Type**</span></span>|<span data-ttu-id="e6eea-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e6eea-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e6eea-114">_section_</span><span class="sxs-lookup"><span data-stu-id="e6eea-114">_section_</span></span> <br/> |<span data-ttu-id="e6eea-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e6eea-115">Required</span></span>  <br/> |<span data-ttu-id="e6eea-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e6eea-116">**String**</span></span> <br/> |<span data-ttu-id="e6eea-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="e6eea-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="e6eea-118">_segmento_</span><span class="sxs-lookup"><span data-stu-id="e6eea-118">_segment_</span></span> <br/> |<span data-ttu-id="e6eea-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="e6eea-119">Optional</span></span>  <br/> |<span data-ttu-id="e6eea-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e6eea-120">**Integer**</span></span> <br/> |<span data-ttu-id="e6eea-121">O segmento baseado em 1 do caminho a ser medido.</span><span class="sxs-lookup"><span data-stu-id="e6eea-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e6eea-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e6eea-122">Return value</span></span>

 <span data-ttu-id="e6eea-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="e6eea-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6eea-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6eea-124">Remarks</span></span>

<span data-ttu-id="e6eea-125">Se não existir _section_ nem _segment_ , o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="e6eea-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="e6eea-126">Se você incluir um valor _segment_ , PATHLENGTH retornará o tamanho desse segmento apenas.</span><span class="sxs-lookup"><span data-stu-id="e6eea-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

