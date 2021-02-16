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
description: Retorna as coordenadas x,y de um ponto no sistema de coordenadas do pai da forma.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414505"
---
# <a name="par-function"></a><span data-ttu-id="521fa-103">Função PAR</span><span class="sxs-lookup"><span data-stu-id="521fa-103">PAR Function</span></span>

<span data-ttu-id="521fa-104">Retorna as  _coordenadas x,y_ de um ponto no sistema de coordenadas do pai da forma.</span><span class="sxs-lookup"><span data-stu-id="521fa-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="521fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="521fa-105">Syntax</span></span>

<span data-ttu-id="521fa-106">PAR(\*\* *ponto* \*\* )</span><span class="sxs-lookup"><span data-stu-id="521fa-106">PAR(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="521fa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="521fa-107">Parameters</span></span>

|<span data-ttu-id="521fa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="521fa-108">**Name**</span></span>|<span data-ttu-id="521fa-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="521fa-109">**Required/Optional**</span></span>|<span data-ttu-id="521fa-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="521fa-110">**Data Type**</span></span>|<span data-ttu-id="521fa-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="521fa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="521fa-112">_point_</span><span class="sxs-lookup"><span data-stu-id="521fa-112">_point_</span></span> <br/> |<span data-ttu-id="521fa-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="521fa-113">Required</span></span>  <br/> |<span data-ttu-id="521fa-114">**Número, Número**</span><span class="sxs-lookup"><span data-stu-id="521fa-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="521fa-115">As coordenadas do ponto do sistema de coordenadas da forma atual.</span><span class="sxs-lookup"><span data-stu-id="521fa-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="521fa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="521fa-116">Remarks</span></span>

<span data-ttu-id="521fa-117">No Microsoft Visio, um ponto é um valor único que incorpora um par de *coordenadas x* e *y.*</span><span class="sxs-lookup"><span data-stu-id="521fa-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="521fa-118">Se a forma estiver em um grupo, seu pai será o grupo.</span><span class="sxs-lookup"><span data-stu-id="521fa-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="521fa-119">Se não estiver em um grupo, seu pai será a página.</span><span class="sxs-lookup"><span data-stu-id="521fa-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="521fa-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="521fa-120">Example</span></span>

<span data-ttu-id="521fa-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="521fa-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="521fa-p102">Nesta expressão, PNT converte um par de coordenadas na forma atual em um ponto. Em seguida, PAR converte o ponto em um par de coordenadas em relação ao canto inferior esquerdo da página ou do grupo que contém a forma atual.</span><span class="sxs-lookup"><span data-stu-id="521fa-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

