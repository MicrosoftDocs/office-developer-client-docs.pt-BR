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
description: Retorna uma polilinha. Essa função é usada na célula a das linhas geométricas PolyLineTo.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772504"
---
# <a name="polyline-function"></a><span data-ttu-id="45fb7-104">Função POLYLINE</span><span class="sxs-lookup"><span data-stu-id="45fb7-104">POLYLINE Function</span></span>

<span data-ttu-id="45fb7-105">Retorna uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="45fb7-105">Returns a polyline.</span></span> <span data-ttu-id="45fb7-106">Essa função é usada na célula a das linhas geométricas PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="45fb7-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="45fb7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45fb7-107">Syntax</span></span>

<span data-ttu-id="45fb7-108">POLILINHA (* * *tipoX* * *, * * *tipoY* * *, * * *x1* * *, * * *y1* * *...)</span><span class="sxs-lookup"><span data-stu-id="45fb7-108">POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="45fb7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45fb7-109">Parameters</span></span>

|<span data-ttu-id="45fb7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="45fb7-110">**Name**</span></span>|<span data-ttu-id="45fb7-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="45fb7-111">**Required/Optional**</span></span>|<span data-ttu-id="45fb7-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="45fb7-112">**Data Type**</span></span>|<span data-ttu-id="45fb7-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="45fb7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="45fb7-114">_tipoX_</span><span class="sxs-lookup"><span data-stu-id="45fb7-114">_xType_</span></span> <br/> |<span data-ttu-id="45fb7-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="45fb7-115">Required</span></span>  <br/> |<span data-ttu-id="45fb7-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="45fb7-116">**Boolean**</span></span> <br/> |<span data-ttu-id="45fb7-117">Especifica como interpretar os dados de entrada de _x_ .</span><span class="sxs-lookup"><span data-stu-id="45fb7-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="45fb7-118">Se _tipoX_ for 0, a entrada _x_-dados serão interpretadas como uma porcentagem da largura.</span><span class="sxs-lookup"><span data-stu-id="45fb7-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="45fb7-119">Se _tipoX_ for 1, a entrada _x_-dados serão interpretadas como uma coordenada local.</span><span class="sxs-lookup"><span data-stu-id="45fb7-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="45fb7-120">_tipoY_</span><span class="sxs-lookup"><span data-stu-id="45fb7-120">_yType_</span></span> <br/> |<span data-ttu-id="45fb7-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="45fb7-121">Required</span></span>  <br/> |<span data-ttu-id="45fb7-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="45fb7-122">**Boolean**</span></span> <br/> |<span data-ttu-id="45fb7-123">Especifica como interpretar o _y_-entrada de dados.</span><span class="sxs-lookup"><span data-stu-id="45fb7-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="45fb7-124">Se _tipoY_ for 0, a entrada _y_-dados serão interpretadas como uma porcentagem da altura.</span><span class="sxs-lookup"><span data-stu-id="45fb7-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="45fb7-125">Se _tipoY_ for 1, a entrada _y_-dados serão interpretadas como uma coordenada local.</span><span class="sxs-lookup"><span data-stu-id="45fb7-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="45fb7-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="45fb7-126">_x1_</span></span> <br/> |<span data-ttu-id="45fb7-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="45fb7-127">Required</span></span>  <br/> |<span data-ttu-id="45fb7-128">**Número**</span><span class="sxs-lookup"><span data-stu-id="45fb7-128">**Number**</span></span> <br/> | <span data-ttu-id="45fb7-129">Um _x_-coordenar.</span><span class="sxs-lookup"><span data-stu-id="45fb7-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="45fb7-130">_Y1_</span><span class="sxs-lookup"><span data-stu-id="45fb7-130">_y1_</span></span> <br/> |<span data-ttu-id="45fb7-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="45fb7-131">Required</span></span>  <br/> |<span data-ttu-id="45fb7-132">**Número**</span><span class="sxs-lookup"><span data-stu-id="45fb7-132">**Number**</span></span> <br/> |<span data-ttu-id="45fb7-133">Um _y_-coordenar.</span><span class="sxs-lookup"><span data-stu-id="45fb7-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45fb7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="45fb7-134">Remarks</span></span>

<span data-ttu-id="45fb7-135">Para cada argumento *x* , deve haver um argumento *y* ; Caso contrário, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="45fb7-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="45fb7-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="45fb7-136">Example</span></span>

<span data-ttu-id="45fb7-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="45fb7-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="45fb7-138">Retornará um retângulo de dimensões usando Width x Height.</span><span class="sxs-lookup"><span data-stu-id="45fb7-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

