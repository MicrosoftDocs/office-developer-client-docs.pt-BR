---
title: Função PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Retorna o número de segmento baseado em 1 na marca de porcentagem especificada ao longo do caminho especificado.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344447"
---
# <a name="pathsegment-function"></a><span data-ttu-id="76243-103">Função PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="76243-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="76243-104">Retorna o número de segmento baseado em 1 na marca de porcentagem especificada ao longo do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="76243-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="76243-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76243-105">Syntax</span></span>

<span data-ttu-id="76243-106">PATHSEGMENT (\* \* *seção* \* \*, \* \* *viagem* \* \*)</span><span class="sxs-lookup"><span data-stu-id="76243-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76243-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76243-107">Parameters</span></span>

|<span data-ttu-id="76243-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="76243-108">**Name**</span></span>|<span data-ttu-id="76243-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="76243-109">**Required/Optional**</span></span>|<span data-ttu-id="76243-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="76243-110">**Data Type**</span></span>|<span data-ttu-id="76243-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="76243-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76243-112">_section_</span><span class="sxs-lookup"><span data-stu-id="76243-112">_section_</span></span> <br/> |<span data-ttu-id="76243-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="76243-113">Required</span></span>  <br/> |<span data-ttu-id="76243-114">**String**</span><span class="sxs-lookup"><span data-stu-id="76243-114">**String**</span></span> <br/> |<span data-ttu-id="76243-115">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="76243-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="76243-116">_transmiti_</span><span class="sxs-lookup"><span data-stu-id="76243-116">_travel_</span></span> <br/> |<span data-ttu-id="76243-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="76243-117">Required</span></span>  <br/> |<span data-ttu-id="76243-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="76243-118">**Double**</span></span> <br/> |<span data-ttu-id="76243-119">O percentual do caminho percorrido, do ponto inicial ao ponto final.</span><span class="sxs-lookup"><span data-stu-id="76243-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="76243-120">Deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="76243-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="76243-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="76243-121">Return value</span></span>

<span data-ttu-id="76243-122">Integer</span><span class="sxs-lookup"><span data-stu-id="76243-122">Integer</span></span>
  

