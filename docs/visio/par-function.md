---
title: Função PAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Retorna a coordenada x, y de um ponto no sistema de coordenadas do pai da forma.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772467"
---
# <a name="par-function"></a><span data-ttu-id="482b1-103">Função PAR</span><span class="sxs-lookup"><span data-stu-id="482b1-103">PAR Function</span></span>

<span data-ttu-id="482b1-104">Retorna as coordenadas _x, y_ de um ponto no sistema de coordenadas do pai da forma.</span><span class="sxs-lookup"><span data-stu-id="482b1-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="482b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="482b1-105">Syntax</span></span>

<span data-ttu-id="482b1-106">PAR (* * *aponte* * *)</span><span class="sxs-lookup"><span data-stu-id="482b1-106">PAR(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="482b1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="482b1-107">Parameters</span></span>

|<span data-ttu-id="482b1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="482b1-108">**Name**</span></span>|<span data-ttu-id="482b1-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="482b1-109">**Required/Optional**</span></span>|<span data-ttu-id="482b1-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="482b1-110">**Data Type**</span></span>|<span data-ttu-id="482b1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="482b1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="482b1-112">_ponto_</span><span class="sxs-lookup"><span data-stu-id="482b1-112">_point_</span></span> <br/> |<span data-ttu-id="482b1-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="482b1-113">Required</span></span>  <br/> |<span data-ttu-id="482b1-114">**Número, Número**</span><span class="sxs-lookup"><span data-stu-id="482b1-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="482b1-115">As coordenadas do ponto do sistema de coordenadas da forma atual.</span><span class="sxs-lookup"><span data-stu-id="482b1-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="482b1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="482b1-116">Remarks</span></span>

<span data-ttu-id="482b1-117">No Microsoft Visio, um ponto é um valor único que incorpora um par de *x* e *y* -coordenadas.</span><span class="sxs-lookup"><span data-stu-id="482b1-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="482b1-118">Se a forma estiver em um grupo, seu pai é o grupo.</span><span class="sxs-lookup"><span data-stu-id="482b1-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="482b1-119">Se a forma não estiver em um grupo, seu pai é a página.</span><span class="sxs-lookup"><span data-stu-id="482b1-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="482b1-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="482b1-120">Example</span></span>

<span data-ttu-id="482b1-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="482b1-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="482b1-p102">Nesta expressão, PNT converte um par de coordenadas na forma atual em um ponto. Em seguida, PAR converte o ponto em um par de coordenadas em relação ao canto inferior esquerdo da página ou do grupo que contém a forma atual.</span><span class="sxs-lookup"><span data-stu-id="482b1-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

