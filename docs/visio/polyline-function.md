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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348273"
---
# <a name="polyline-function"></a><span data-ttu-id="a5904-104">Função POLYLINE</span><span class="sxs-lookup"><span data-stu-id="a5904-104">POLYLINE Function</span></span>

<span data-ttu-id="a5904-105">Retorna uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="a5904-105">Returns a polyline.</span></span> <span data-ttu-id="a5904-106">Essa função é usada na célula A de linhas geométricas de poliLinhato.</span><span class="sxs-lookup"><span data-stu-id="a5904-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a5904-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5904-107">Syntax</span></span>

<span data-ttu-id="a5904-108">POLYLINE (\* \* *xType* \* \*, \* \* *yType* \* \*, \* \* *X1* \* \*, \* \* *Y1* \* \*...)</span><span class="sxs-lookup"><span data-stu-id="a5904-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a5904-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5904-109">Parameters</span></span>

|<span data-ttu-id="a5904-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a5904-110">**Name**</span></span>|<span data-ttu-id="a5904-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a5904-111">**Required/Optional**</span></span>|<span data-ttu-id="a5904-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a5904-112">**Data Type**</span></span>|<span data-ttu-id="a5904-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a5904-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a5904-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="a5904-114">_xType_</span></span> <br/> |<span data-ttu-id="a5904-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a5904-115">Required</span></span>  <br/> |<span data-ttu-id="a5904-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a5904-116">**Boolean**</span></span> <br/> |<span data-ttu-id="a5904-117">Especifica como interpretar os dados de entrada _x_ .</span><span class="sxs-lookup"><span data-stu-id="a5904-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="a5904-118">Se _xType_ for 0, os dados de entrada _x_serão interpretados como uma porcentagem de largura.</span><span class="sxs-lookup"><span data-stu-id="a5904-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="a5904-119">Se _xType_ for 1, os dados _x_-Input serão interpretados como uma coordenada local.</span><span class="sxs-lookup"><span data-stu-id="a5904-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="a5904-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="a5904-120">_yType_</span></span> <br/> |<span data-ttu-id="a5904-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a5904-121">Required</span></span>  <br/> |<span data-ttu-id="a5904-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a5904-122">**Boolean**</span></span> <br/> |<span data-ttu-id="a5904-123">Especifica como interpretar os dados de entrada _y_.</span><span class="sxs-lookup"><span data-stu-id="a5904-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="a5904-124">Se _yType_ for 0, os dados _y_de entrada serão interpretados como uma porcentagem da altura.</span><span class="sxs-lookup"><span data-stu-id="a5904-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="a5904-125">Se _yType_ for 1, os dados _y_de entrada serão interpretados como uma coordenada local.</span><span class="sxs-lookup"><span data-stu-id="a5904-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="a5904-126">_X1_</span><span class="sxs-lookup"><span data-stu-id="a5904-126">_x1_</span></span> <br/> |<span data-ttu-id="a5904-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a5904-127">Required</span></span>  <br/> |<span data-ttu-id="a5904-128">**Número**</span><span class="sxs-lookup"><span data-stu-id="a5904-128">**Number**</span></span> <br/> | <span data-ttu-id="a5904-129">Uma coordenada _x_.</span><span class="sxs-lookup"><span data-stu-id="a5904-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="a5904-130">_a1_</span><span class="sxs-lookup"><span data-stu-id="a5904-130">_y1_</span></span> <br/> |<span data-ttu-id="a5904-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a5904-131">Required</span></span>  <br/> |<span data-ttu-id="a5904-132">**Número**</span><span class="sxs-lookup"><span data-stu-id="a5904-132">**Number**</span></span> <br/> |<span data-ttu-id="a5904-133">Uma coordenada _y_.</span><span class="sxs-lookup"><span data-stu-id="a5904-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5904-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5904-134">Remarks</span></span>

<span data-ttu-id="a5904-135">Para cada argumento *x* , deve haver um argumento *y* ; caso contrário, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="a5904-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a5904-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a5904-136">Example</span></span>

<span data-ttu-id="a5904-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="a5904-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="a5904-138">Retornará um retângulo de dimensões usando Width x Height.</span><span class="sxs-lookup"><span data-stu-id="a5904-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

