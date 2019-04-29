---
title: Função POLYLINE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Retorna uma polilinha. Essa função é usada na célula A de linhas geométricas de poliLinhato.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426293"
---
# <a name="polyline-function"></a><span data-ttu-id="daac3-104">Função POLYLINE</span><span class="sxs-lookup"><span data-stu-id="daac3-104">POLYLINE Function</span></span>

<span data-ttu-id="daac3-105">Retorna uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="daac3-105">Returns a polyline.</span></span> <span data-ttu-id="daac3-106">Essa função é usada na célula A de linhas geométricas de poliLinhato.</span><span class="sxs-lookup"><span data-stu-id="daac3-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="daac3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daac3-107">Syntax</span></span>

<span data-ttu-id="daac3-108">POLYLINE (\* \* *xType* \* \*, \* \* *yType* \* \*, \* \* *X1* \* \*, \* \* *Y1* \* \*...)</span><span class="sxs-lookup"><span data-stu-id="daac3-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="daac3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daac3-109">Parameters</span></span>

|<span data-ttu-id="daac3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="daac3-110">**Name**</span></span>|<span data-ttu-id="daac3-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="daac3-111">**Required/Optional**</span></span>|<span data-ttu-id="daac3-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="daac3-112">**Data Type**</span></span>|<span data-ttu-id="daac3-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="daac3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="daac3-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="daac3-114">_xType_</span></span> <br/> |<span data-ttu-id="daac3-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="daac3-115">Required</span></span>  <br/> |<span data-ttu-id="daac3-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="daac3-116">**Boolean**</span></span> <br/> |<span data-ttu-id="daac3-117">Especifica como interpretar os dados de entrada _x_ .</span><span class="sxs-lookup"><span data-stu-id="daac3-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="daac3-118">Se _xType_ for 0, os dados de entrada _x_serão interpretados como uma porcentagem de largura.</span><span class="sxs-lookup"><span data-stu-id="daac3-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="daac3-119">Se _xType_ for 1, os dados _x_-Input serão interpretados como uma coordenada local.</span><span class="sxs-lookup"><span data-stu-id="daac3-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="daac3-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="daac3-120">_yType_</span></span> <br/> |<span data-ttu-id="daac3-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="daac3-121">Required</span></span>  <br/> |<span data-ttu-id="daac3-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="daac3-122">**Boolean**</span></span> <br/> |<span data-ttu-id="daac3-123">Especifica como interpretar os dados de entrada _y_.</span><span class="sxs-lookup"><span data-stu-id="daac3-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="daac3-124">Se _yType_ for 0, os dados _y_de entrada serão interpretados como uma porcentagem da altura.</span><span class="sxs-lookup"><span data-stu-id="daac3-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="daac3-125">Se _yType_ for 1, os dados _y_de entrada serão interpretados como uma coordenada local.</span><span class="sxs-lookup"><span data-stu-id="daac3-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="daac3-126">_X1_</span><span class="sxs-lookup"><span data-stu-id="daac3-126">_x1_</span></span> <br/> |<span data-ttu-id="daac3-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="daac3-127">Required</span></span>  <br/> |<span data-ttu-id="daac3-128">**Número**</span><span class="sxs-lookup"><span data-stu-id="daac3-128">**Number**</span></span> <br/> | <span data-ttu-id="daac3-129">Uma coordenada _x_.</span><span class="sxs-lookup"><span data-stu-id="daac3-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="daac3-130">_a1_</span><span class="sxs-lookup"><span data-stu-id="daac3-130">_y1_</span></span> <br/> |<span data-ttu-id="daac3-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="daac3-131">Required</span></span>  <br/> |<span data-ttu-id="daac3-132">**Número**</span><span class="sxs-lookup"><span data-stu-id="daac3-132">**Number**</span></span> <br/> |<span data-ttu-id="daac3-133">Uma coordenada _y_.</span><span class="sxs-lookup"><span data-stu-id="daac3-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daac3-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="daac3-134">Remarks</span></span>

<span data-ttu-id="daac3-135">Para cada argumento *x* , deve haver um argumento *y* ; caso contrário, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="daac3-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="daac3-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="daac3-136">Example</span></span>

<span data-ttu-id="daac3-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="daac3-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="daac3-138">Retornará um retângulo de dimensões usando Width x Height.</span><span class="sxs-lookup"><span data-stu-id="daac3-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

