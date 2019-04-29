---
title: Função DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427014"
---
# <a name="disttopath-function"></a><span data-ttu-id="60ad8-103">Função DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="60ad8-103">DISTTOPATH Function</span></span>

<span data-ttu-id="60ad8-104">Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.</span><span class="sxs-lookup"><span data-stu-id="60ad8-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="60ad8-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="60ad8-105">Version Information</span></span>

<span data-ttu-id="60ad8-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="60ad8-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="60ad8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60ad8-107">Syntax</span></span>

<span data-ttu-id="60ad8-108">DISTTOPATH (\* \* *seção* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="60ad8-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="60ad8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60ad8-109">Parameters</span></span>

|<span data-ttu-id="60ad8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="60ad8-110">**Name**</span></span>|<span data-ttu-id="60ad8-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="60ad8-111">**Required/Optional**</span></span>|<span data-ttu-id="60ad8-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="60ad8-112">**Data Type**</span></span>|<span data-ttu-id="60ad8-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="60ad8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="60ad8-114">_section_</span><span class="sxs-lookup"><span data-stu-id="60ad8-114">_section_</span></span> <br/> |<span data-ttu-id="60ad8-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="60ad8-115">Required</span></span>  <br/> |<span data-ttu-id="60ad8-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60ad8-116">**String**</span></span> <br/> |<span data-ttu-id="60ad8-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="60ad8-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="60ad8-118">_x_</span><span class="sxs-lookup"><span data-stu-id="60ad8-118">_x_</span></span> <br/> |<span data-ttu-id="60ad8-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="60ad8-119">Required</span></span>  <br/> |<span data-ttu-id="60ad8-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="60ad8-120">**Double**</span></span> <br/> |<span data-ttu-id="60ad8-121">A coordenada _x_do ponto.</span><span class="sxs-lookup"><span data-stu-id="60ad8-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="60ad8-122">_y_</span><span class="sxs-lookup"><span data-stu-id="60ad8-122">_y_</span></span> <br/> |<span data-ttu-id="60ad8-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="60ad8-123">Required</span></span>  <br/> |<span data-ttu-id="60ad8-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="60ad8-124">**Double**</span></span> <br/> |<span data-ttu-id="60ad8-125">A coordenada _y_do ponto.</span><span class="sxs-lookup"><span data-stu-id="60ad8-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="60ad8-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="60ad8-126">Return value</span></span>

 <span data-ttu-id="60ad8-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="60ad8-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60ad8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="60ad8-128">Remarks</span></span>

<span data-ttu-id="60ad8-129">O Microsoft Visio retornará #REF!</span><span class="sxs-lookup"><span data-stu-id="60ad8-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="60ad8-130">se a _seção_ não existir.</span><span class="sxs-lookup"><span data-stu-id="60ad8-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="60ad8-131">O valor retornado será positivo se o ponto estiver à esquerda da direção da viagem e negativo caso esteja à direita.</span><span class="sxs-lookup"><span data-stu-id="60ad8-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

