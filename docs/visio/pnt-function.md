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
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772557"
---
# <a name="pnt-function"></a><span data-ttu-id="5113f-103">Função PNT</span><span class="sxs-lookup"><span data-stu-id="5113f-103">PNT Function</span></span>

<span data-ttu-id="5113f-104">Retorna o ponto representado pelas coordenadas _x_ e _y_ como um único valor.</span><span class="sxs-lookup"><span data-stu-id="5113f-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5113f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5113f-105">Syntax</span></span>

<span data-ttu-id="5113f-106">PNT (* * *x, y* * *)</span><span class="sxs-lookup"><span data-stu-id="5113f-106">PNT(** *x,y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5113f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5113f-107">Parameters</span></span>

|<span data-ttu-id="5113f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5113f-108">**Name**</span></span>|<span data-ttu-id="5113f-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5113f-109">**Required/Optional**</span></span>|<span data-ttu-id="5113f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5113f-110">**Data Type**</span></span>|<span data-ttu-id="5113f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5113f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5113f-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="5113f-112">_x,y_</span></span> <br/> |<span data-ttu-id="5113f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5113f-113">Required</span></span>  <br/> |<span data-ttu-id="5113f-114">**Número, Número**</span><span class="sxs-lookup"><span data-stu-id="5113f-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="5113f-115">As coordenadas do ponto do sistema de coordenadas da forma atual.</span><span class="sxs-lookup"><span data-stu-id="5113f-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5113f-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5113f-116">Return value</span></span>

<span data-ttu-id="5113f-117">Ponto</span><span class="sxs-lookup"><span data-stu-id="5113f-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5113f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5113f-118">Remarks</span></span>

<span data-ttu-id="5113f-119">Convertendo coordenadas para pontos permite alterar a geometria de uma forma sem precisar manipular *x* e *y* -coordena separadamente.</span><span class="sxs-lookup"><span data-stu-id="5113f-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5113f-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5113f-120">Example</span></span>

<span data-ttu-id="5113f-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="5113f-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="5113f-122">Retornará o ponto representado por PinX e PinY.</span><span class="sxs-lookup"><span data-stu-id="5113f-122">Returns the point represented by PinX and PinY.</span></span> 
  

