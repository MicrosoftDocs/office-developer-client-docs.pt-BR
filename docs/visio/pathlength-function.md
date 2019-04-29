---
title: Função PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Retorna o tamanho do caminho definido na seção Geometry especificada.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405846"
---
# <a name="pathlength-function"></a><span data-ttu-id="6fb7f-103">Função PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="6fb7f-103">PATHLENGTH Function</span></span>

<span data-ttu-id="6fb7f-104">Retorna o tamanho do caminho definido na seção Geometry especificada.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="6fb7f-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="6fb7f-105">Version Information</span></span>

<span data-ttu-id="6fb7f-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="6fb7f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6fb7f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fb7f-107">Syntax</span></span>

<span data-ttu-id="6fb7f-108">PATHLENGTH (\* \* *seção* \* \* \* \* *[, segmento]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6fb7f-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6fb7f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fb7f-109">Parameters</span></span>

|<span data-ttu-id="6fb7f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-110">**Name**</span></span>|<span data-ttu-id="6fb7f-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-111">**Required/Optional**</span></span>|<span data-ttu-id="6fb7f-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-112">**Data Type**</span></span>|<span data-ttu-id="6fb7f-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6fb7f-114">_section_</span><span class="sxs-lookup"><span data-stu-id="6fb7f-114">_section_</span></span> <br/> |<span data-ttu-id="6fb7f-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6fb7f-115">Required</span></span>  <br/> |<span data-ttu-id="6fb7f-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-116">**String**</span></span> <br/> |<span data-ttu-id="6fb7f-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="6fb7f-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="6fb7f-118">_segmento_</span><span class="sxs-lookup"><span data-stu-id="6fb7f-118">_segment_</span></span> <br/> |<span data-ttu-id="6fb7f-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="6fb7f-119">Optional</span></span>  <br/> |<span data-ttu-id="6fb7f-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-120">**Integer**</span></span> <br/> |<span data-ttu-id="6fb7f-121">O segmento baseado em 1 do caminho a ser medido.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6fb7f-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6fb7f-122">Return value</span></span>

 <span data-ttu-id="6fb7f-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6fb7f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fb7f-124">Remarks</span></span>

<span data-ttu-id="6fb7f-125">Se a _seção_ ou o _segmento_ não existir, o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="6fb7f-126">Se você incluir um valor de _segmento_ , PATHLENGTH retornará somente o comprimento desse segmento.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

