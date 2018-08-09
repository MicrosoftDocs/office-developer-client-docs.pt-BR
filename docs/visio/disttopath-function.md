---
title: Função DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771747"
---
# <a name="disttopath-function"></a><span data-ttu-id="5afac-103">Função DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="5afac-103">DISTTOPATH Function</span></span>

<span data-ttu-id="5afac-104">Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.</span><span class="sxs-lookup"><span data-stu-id="5afac-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5afac-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="5afac-105">Version Information</span></span>

<span data-ttu-id="5afac-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="5afac-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5afac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5afac-107">Syntax</span></span>

<span data-ttu-id="5afac-108">DISTTOPATH (* * *seção* * *, * * *x* * *, * * *y* * *)</span><span class="sxs-lookup"><span data-stu-id="5afac-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5afac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5afac-109">Parameters</span></span>

|<span data-ttu-id="5afac-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5afac-110">**Name**</span></span>|<span data-ttu-id="5afac-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5afac-111">**Required/Optional**</span></span>|<span data-ttu-id="5afac-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5afac-112">**Data Type**</span></span>|<span data-ttu-id="5afac-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5afac-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5afac-114">_section_</span><span class="sxs-lookup"><span data-stu-id="5afac-114">_section_</span></span> <br/> |<span data-ttu-id="5afac-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5afac-115">Required</span></span>  <br/> |<span data-ttu-id="5afac-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5afac-116">**String**</span></span> <br/> |<span data-ttu-id="5afac-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="5afac-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="5afac-118">_x_</span><span class="sxs-lookup"><span data-stu-id="5afac-118">_x_</span></span> <br/> |<span data-ttu-id="5afac-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5afac-119">Required</span></span>  <br/> |<span data-ttu-id="5afac-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="5afac-120">**Double**</span></span> <br/> |<span data-ttu-id="5afac-121">_X_-coordenadas do ponto.</span><span class="sxs-lookup"><span data-stu-id="5afac-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="5afac-122">_y_</span><span class="sxs-lookup"><span data-stu-id="5afac-122">_y_</span></span> <br/> |<span data-ttu-id="5afac-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5afac-123">Required</span></span>  <br/> |<span data-ttu-id="5afac-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="5afac-124">**Double**</span></span> <br/> |<span data-ttu-id="5afac-125">_Y_-coordenadas do ponto.</span><span class="sxs-lookup"><span data-stu-id="5afac-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5afac-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5afac-126">Return value</span></span>

 <span data-ttu-id="5afac-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="5afac-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5afac-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5afac-128">Remarks</span></span>

<span data-ttu-id="5afac-129">O Microsoft Visio retornará #REF!</span><span class="sxs-lookup"><span data-stu-id="5afac-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="5afac-130">Se não existir _section_ .</span><span class="sxs-lookup"><span data-stu-id="5afac-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="5afac-131">O valor retornado será positivo se o ponto estiver à esquerda da direção da viagem e negativo caso esteja à direita.</span><span class="sxs-lookup"><span data-stu-id="5afac-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

