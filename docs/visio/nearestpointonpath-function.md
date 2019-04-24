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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319716"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="e134d-103">Função NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="e134d-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="e134d-104">Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="e134d-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e134d-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="e134d-105">Version Information</span></span>

<span data-ttu-id="e134d-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="e134d-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e134d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e134d-107">Syntax</span></span>

<span data-ttu-id="e134d-108">NEARESTPOINTONPATH (\* \* *seção* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e134d-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e134d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e134d-109">Parameters</span></span>

|<span data-ttu-id="e134d-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e134d-110">**Name**</span></span>|<span data-ttu-id="e134d-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="e134d-111">**Required/Optional**</span></span>|<span data-ttu-id="e134d-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e134d-112">**Data Type**</span></span>|<span data-ttu-id="e134d-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e134d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e134d-114">_section_</span><span class="sxs-lookup"><span data-stu-id="e134d-114">_section_</span></span> <br/> |<span data-ttu-id="e134d-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e134d-115">Required</span></span>  <br/> |<span data-ttu-id="e134d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e134d-116">**String**</span></span> <br/> |<span data-ttu-id="e134d-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="e134d-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="e134d-118">_x_</span><span class="sxs-lookup"><span data-stu-id="e134d-118">_x_</span></span> <br/> |<span data-ttu-id="e134d-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e134d-119">Required</span></span>  <br/> |<span data-ttu-id="e134d-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="e134d-120">**Double**</span></span> <br/> |<span data-ttu-id="e134d-121">A coordenada _x_do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="e134d-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="e134d-122">_y_</span><span class="sxs-lookup"><span data-stu-id="e134d-122">_y_</span></span> <br/> |<span data-ttu-id="e134d-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e134d-123">Required</span></span>  <br/> |<span data-ttu-id="e134d-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="e134d-124">**Double**</span></span> <br/> |<span data-ttu-id="e134d-125">A coordenada _y_do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="e134d-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e134d-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e134d-126">Return value</span></span>

 <span data-ttu-id="e134d-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="e134d-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e134d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e134d-128">Remarks</span></span>

<span data-ttu-id="e134d-129">Se a _seção_ não existir, o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="e134d-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

