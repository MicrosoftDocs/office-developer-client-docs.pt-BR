---
title: Linha ArcTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Contém as coordenadas x e y e a curva de um arco circular.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341402"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="1b21d-103">Linha ArcTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="1b21d-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="1b21d-104">Contém as coordenadas *x* e *y* e a curva de um arco circular.</span><span class="sxs-lookup"><span data-stu-id="1b21d-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="1b21d-105">Uma linha ArcTo contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b21d-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="1b21d-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1b21d-106">**Cell**</span></span>|<span data-ttu-id="1b21d-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b21d-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b21d-108">X</span><span class="sxs-lookup"><span data-stu-id="1b21d-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="1b21d-109">A coordenada *x* do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="1b21d-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="1b21d-110">Y</span><span class="sxs-lookup"><span data-stu-id="1b21d-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="1b21d-111">A coordenada *y* do vértice final de um arco.</span><span class="sxs-lookup"><span data-stu-id="1b21d-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="1b21d-112">A</span><span class="sxs-lookup"><span data-stu-id="1b21d-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="1b21d-113">A distância do ponto médio de um arco até o ponto médio de sua corda.</span><span class="sxs-lookup"><span data-stu-id="1b21d-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b21d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b21d-114">Remarks</span></span>

<span data-ttu-id="1b21d-p101">Os arcos desenhados no Visio são elípticos, mesmo se baseados em um círculo. Por padrão, os arcos desenhados são representados por uma linha EllipticalArcTo em uma janela ShapeSheet. Para mostrar uma linha ArcTo em uma janela ShapeSheet, desenhe um arco e depois altere o tipo de linha EllipticalArcTo para uma linha ArcTo; na verdade, você está alterando um arco elíptico para um arco circular.</span><span class="sxs-lookup"><span data-stu-id="1b21d-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="1b21d-118">Para alterar um tipo de linha, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="1b21d-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

