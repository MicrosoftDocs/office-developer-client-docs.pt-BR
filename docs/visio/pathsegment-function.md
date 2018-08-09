---
title: Função PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Retorna o número de segmento baseado em 1 na marca de percentual especificado no caminho especificado.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772478"
---
# <a name="pathsegment-function"></a><span data-ttu-id="af682-103">Função PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="af682-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="af682-104">Retorna o número de segmento baseado em 1 na marca de percentual especificado no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="af682-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="af682-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af682-105">Syntax</span></span>

<span data-ttu-id="af682-106">PATHSEGMENT (* * *seção* * *, * * *de viagem* * *)</span><span class="sxs-lookup"><span data-stu-id="af682-106">PATHSEGMENT(** *section* **, ** *travel* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="af682-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af682-107">Parameters</span></span>

|<span data-ttu-id="af682-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="af682-108">**Name**</span></span>|<span data-ttu-id="af682-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="af682-109">**Required/Optional**</span></span>|<span data-ttu-id="af682-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="af682-110">**Data Type**</span></span>|<span data-ttu-id="af682-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="af682-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="af682-112">_section_</span><span class="sxs-lookup"><span data-stu-id="af682-112">_section_</span></span> <br/> |<span data-ttu-id="af682-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="af682-113">Required</span></span>  <br/> |<span data-ttu-id="af682-114">**String**</span><span class="sxs-lookup"><span data-stu-id="af682-114">**String**</span></span> <br/> |<span data-ttu-id="af682-115">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="af682-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="af682-116">_viagem_</span><span class="sxs-lookup"><span data-stu-id="af682-116">_travel_</span></span> <br/> |<span data-ttu-id="af682-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="af682-117">Required</span></span>  <br/> |<span data-ttu-id="af682-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="af682-118">**Double**</span></span> <br/> |<span data-ttu-id="af682-p101">O percentual do caminho percorrido, do ponto inicial ao ponto final. Deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="af682-p101">The percentage of the path traversed, from the begin point to the end point. Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="af682-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="af682-121">Return value</span></span>

<span data-ttu-id="af682-122">Inteiro</span><span class="sxs-lookup"><span data-stu-id="af682-122">Integer</span></span>
  

