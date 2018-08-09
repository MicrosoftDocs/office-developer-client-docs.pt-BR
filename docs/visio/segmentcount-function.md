---
title: Função SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Retorna o número de segmentos de linha que formam o caminho.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772868"
---
# <a name="segmentcount-function"></a><span data-ttu-id="f8aec-103">Função SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8aec-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="f8aec-104">Retorna o número de segmentos de linha que formam o caminho.</span><span class="sxs-lookup"><span data-stu-id="f8aec-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f8aec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8aec-105">Syntax</span></span>

<span data-ttu-id="f8aec-106">SEGMENTCOUNT (* * *pathRef* * *)</span><span class="sxs-lookup"><span data-stu-id="f8aec-106">SEGMENTCOUNT(** *pathRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f8aec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8aec-107">Parameters</span></span>

|<span data-ttu-id="f8aec-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8aec-108">**Name**</span></span>|<span data-ttu-id="f8aec-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f8aec-109">**Required/Optional**</span></span>|<span data-ttu-id="f8aec-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f8aec-110">**Data Type**</span></span>|<span data-ttu-id="f8aec-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f8aec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f8aec-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="f8aec-112">_pathRef_</span></span> <br/> |<span data-ttu-id="f8aec-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f8aec-113">Required</span></span>  <br/> |<span data-ttu-id="f8aec-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="f8aec-114">**Integer**</span></span> <br/> |<span data-ttu-id="f8aec-115">A seção Geometry que representa o caminho, especificada por uma referência à célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="f8aec-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f8aec-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f8aec-116">Return value</span></span>

<span data-ttu-id="f8aec-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="f8aec-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8aec-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8aec-118">Remarks</span></span>

<span data-ttu-id="f8aec-119">Saltos de linha não são incluídos no número total de segmentos retornados.</span><span class="sxs-lookup"><span data-stu-id="f8aec-119">Line jumps are not included in the total number of segments returned.</span></span>
  

