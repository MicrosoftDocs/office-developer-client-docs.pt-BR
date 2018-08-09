---
title: Linha PolylineTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Contém x e y-coordenadas do último ponto de uma polilinha e uma fórmula de polilinha.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772503"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="9829f-103">Linha PolylineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="9829f-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="9829f-104">Contém *x* e *y* -coordenadas do último ponto de uma polilinha e uma fórmula de polilinha.</span><span class="sxs-lookup"><span data-stu-id="9829f-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="9829f-105">Uma linha PolylineTo contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="9829f-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="9829f-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="9829f-106">**Cell**</span></span>|<span data-ttu-id="9829f-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9829f-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9829f-108">X</span><span class="sxs-lookup"><span data-stu-id="9829f-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="9829f-109">*X* -coordenadas do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="9829f-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="9829f-110">Y</span><span class="sxs-lookup"><span data-stu-id="9829f-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="9829f-111">*Y* -coordenadas do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="9829f-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="9829f-112">A</span><span class="sxs-lookup"><span data-stu-id="9829f-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="9829f-113">A fórmula da polilinha.</span><span class="sxs-lookup"><span data-stu-id="9829f-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9829f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9829f-114">Remarks</span></span>

<span data-ttu-id="9829f-p101">Linhas representadas como uma linha PolylineTo são equivalentes a linhas representadas como uma sequência de linhas LineTo, mas uma linha PolylineTo é mais eficiente. Você pode alterar uma linha PolylineTo para uma linha LineTo de forma que seja possível ver a geometria da forma facilmente. Para fazer isso, clique com o botão direito do mouse na linha PolylineTo e clique em **Expandir Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="9829f-p101">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient. You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry. To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="9829f-118">Para alterar um tipo de linha para uma linha PolylineTo, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="9829f-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

