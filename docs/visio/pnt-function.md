---
title: Função PNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Retorna o ponto representado pelas coordenadas x e y como um único valor.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435709"
---
# <a name="pnt-function"></a><span data-ttu-id="36ce9-103">Função PNT</span><span class="sxs-lookup"><span data-stu-id="36ce9-103">PNT Function</span></span>

<span data-ttu-id="36ce9-104">Retorna o ponto representado pelas coordenadas _x_ e _y_ como um único valor.</span><span class="sxs-lookup"><span data-stu-id="36ce9-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36ce9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36ce9-105">Syntax</span></span>

<span data-ttu-id="36ce9-106">PNT (\* \* *x, y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="36ce9-106">PNT(\*\* *x,y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="36ce9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36ce9-107">Parameters</span></span>

|<span data-ttu-id="36ce9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="36ce9-108">**Name**</span></span>|<span data-ttu-id="36ce9-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="36ce9-109">**Required/Optional**</span></span>|<span data-ttu-id="36ce9-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="36ce9-110">**Data Type**</span></span>|<span data-ttu-id="36ce9-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36ce9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="36ce9-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="36ce9-112">_x,y_</span></span> <br/> |<span data-ttu-id="36ce9-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="36ce9-113">Required</span></span>  <br/> |<span data-ttu-id="36ce9-114">**Número, Número**</span><span class="sxs-lookup"><span data-stu-id="36ce9-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="36ce9-115">As coordenadas do ponto do sistema de coordenadas da forma atual.</span><span class="sxs-lookup"><span data-stu-id="36ce9-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="36ce9-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="36ce9-116">Return value</span></span>

<span data-ttu-id="36ce9-117">Ponto</span><span class="sxs-lookup"><span data-stu-id="36ce9-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36ce9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="36ce9-118">Remarks</span></span>

<span data-ttu-id="36ce9-119">A conversão de coordenadas em pontos permite que você altere a geometria de uma forma sem precisar manipular as coordenadas *x* e *y* separadamente.</span><span class="sxs-lookup"><span data-stu-id="36ce9-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="36ce9-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="36ce9-120">Example</span></span>

<span data-ttu-id="36ce9-121">PNT (PinX, PinY)</span><span class="sxs-lookup"><span data-stu-id="36ce9-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="36ce9-122">Retornará o ponto representado por PinX e PinY.</span><span class="sxs-lookup"><span data-stu-id="36ce9-122">Returns the point represented by PinX and PinY.</span></span> 
  

