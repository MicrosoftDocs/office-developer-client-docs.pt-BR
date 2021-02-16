---
title: Função NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407330"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="2e3c7-103">Função NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="2e3c7-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="2e3c7-104">Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="2e3c7-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="2e3c7-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="2e3c7-105">Version Information</span></span>

<span data-ttu-id="2e3c7-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="2e3c7-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2e3c7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e3c7-107">Syntax</span></span>

<span data-ttu-id="2e3c7-108">NEARESTPOINTONPATH(\*\* *seção* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2e3c7-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e3c7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e3c7-109">Parameters</span></span>

|<span data-ttu-id="2e3c7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-110">**Name**</span></span>|<span data-ttu-id="2e3c7-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-111">**Required/Optional**</span></span>|<span data-ttu-id="2e3c7-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-112">**Data Type**</span></span>|<span data-ttu-id="2e3c7-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e3c7-114">_section_</span><span class="sxs-lookup"><span data-stu-id="2e3c7-114">_section_</span></span> <br/> |<span data-ttu-id="2e3c7-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2e3c7-115">Required</span></span>  <br/> |<span data-ttu-id="2e3c7-116">**String**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-116">**String**</span></span> <br/> |<span data-ttu-id="2e3c7-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="2e3c7-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="2e3c7-118">_x_</span><span class="sxs-lookup"><span data-stu-id="2e3c7-118">_x_</span></span> <br/> |<span data-ttu-id="2e3c7-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2e3c7-119">Required</span></span>  <br/> |<span data-ttu-id="2e3c7-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-120">**Double**</span></span> <br/> |<span data-ttu-id="2e3c7-121">A  _coordenada x_ do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="2e3c7-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="2e3c7-122">_y_</span><span class="sxs-lookup"><span data-stu-id="2e3c7-122">_y_</span></span> <br/> |<span data-ttu-id="2e3c7-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2e3c7-123">Required</span></span>  <br/> |<span data-ttu-id="2e3c7-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-124">**Double**</span></span> <br/> |<span data-ttu-id="2e3c7-125">A  _coordenada y_ do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="2e3c7-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2e3c7-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2e3c7-126">Return value</span></span>

 <span data-ttu-id="2e3c7-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="2e3c7-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e3c7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e3c7-128">Remarks</span></span>

<span data-ttu-id="2e3c7-129">Se  _a_ seção não existir, o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="2e3c7-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

