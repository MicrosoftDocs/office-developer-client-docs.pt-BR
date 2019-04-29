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
description: Contém as coordenadas x e y do último ponto de uma polilinha e uma fórmula de polilinha.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439461"
---
# <a name="polylineto-row-geometry-section"></a><span data-ttu-id="835da-103">Linha PolylineTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="835da-103">PolylineTo Row (Geometry Section)</span></span>

<span data-ttu-id="835da-104">Contém as coordenadas *x* e *y* do último ponto de uma polilinha e uma fórmula de polilinha.</span><span class="sxs-lookup"><span data-stu-id="835da-104">Contains  *x*  - and  *y*  -coordinates of the last point of a polyline and a polyline formula.</span></span> 
  
<span data-ttu-id="835da-105">Uma linha PolylineTo contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="835da-105">A PolylineTo row contains the following cells.</span></span>
  
|<span data-ttu-id="835da-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="835da-106">**Cell**</span></span>|<span data-ttu-id="835da-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="835da-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="835da-108">X</span><span class="sxs-lookup"><span data-stu-id="835da-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="835da-109">A coordenada *x* do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="835da-109">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="835da-110">Y</span><span class="sxs-lookup"><span data-stu-id="835da-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="835da-111">A coordenada *y* do vértice final de uma polilinha.</span><span class="sxs-lookup"><span data-stu-id="835da-111">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="835da-112">A</span><span class="sxs-lookup"><span data-stu-id="835da-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="835da-113">A fórmula da polilinha.</span><span class="sxs-lookup"><span data-stu-id="835da-113">The polyline formula.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="835da-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="835da-114">Remarks</span></span>

<span data-ttu-id="835da-p101">Linhas representadas como uma linha PolylineTo são equivalentes a linhas representadas como uma sequência de linhas LineTo, mas uma linha PolylineTo é mais eficiente. Você pode alterar uma linha PolylineTo para uma linha LineTo de forma que seja possível ver a geometria da forma facilmente. Para fazer isso, clique com o botão direito do mouse na linha PolylineTo e clique em **Expandir Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="835da-p101">Lines represented as a Polyline row are equivalent to lines represented as a sequence of LineTo rows, but a Polyline row is more efficient. You can change a PolylineTo row to a LineTo row so you can easily see the shape geometry. To do this, right-click the PolylineTo row, and then click **Expand Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="835da-118">Para alterar um tipo de linha para uma linha PolylineTo, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="835da-118">To change a row type to a PolylineTo row, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

