---
title: Função SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Retorna o número de segmentos de linha que formam o caminho.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326037"
---
# <a name="segmentcount-function"></a><span data-ttu-id="e947d-103">Função SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="e947d-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="e947d-104">Retorna o número de segmentos de linha que formam o caminho.</span><span class="sxs-lookup"><span data-stu-id="e947d-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e947d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e947d-105">Syntax</span></span>

<span data-ttu-id="e947d-106">SEGMENTCOUNT (\* \* *pathRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e947d-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e947d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e947d-107">Parameters</span></span>

|<span data-ttu-id="e947d-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e947d-108">**Name**</span></span>|<span data-ttu-id="e947d-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="e947d-109">**Required/Optional**</span></span>|<span data-ttu-id="e947d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e947d-110">**Data Type**</span></span>|<span data-ttu-id="e947d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e947d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e947d-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="e947d-112">_pathRef_</span></span> <br/> |<span data-ttu-id="e947d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e947d-113">Required</span></span>  <br/> |<span data-ttu-id="e947d-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e947d-114">**Integer**</span></span> <br/> |<span data-ttu-id="e947d-115">A seção Geometry que representa o caminho, especificada por uma referência à célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="e947d-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e947d-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e947d-116">Return value</span></span>

<span data-ttu-id="e947d-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="e947d-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e947d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e947d-118">Remarks</span></span>

<span data-ttu-id="e947d-119">Saltos de linha não são incluídos no número total de segmentos retornados.</span><span class="sxs-lookup"><span data-stu-id="e947d-119">Line jumps are not included in the total number of segments returned.</span></span>
  

