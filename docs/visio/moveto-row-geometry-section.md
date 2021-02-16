---
title: Linha MoveTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contém as coordenadas x e y do primeiro vértice de uma forma ou representa as coordenadas x e y do primeiro vértice após uma quebra em um caminho.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429695"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="5a4b9-103">Linha MoveTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="5a4b9-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="5a4b9-104">Contém as coordenadas  *x*  e  *y*  do primeiro vértice de uma forma ou representa as coordenadas  *x*  e  *y*  do primeiro vértice após uma quebra em um caminho.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="5a4b9-105">Uma **linha MoveTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="5a4b9-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="5a4b9-106">**Cell**</span></span>|<span data-ttu-id="5a4b9-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5a4b9-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a4b9-108">X</span><span class="sxs-lookup"><span data-stu-id="5a4b9-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="5a4b9-109">Se a **linha MoveTo** for a primeira linha da seção, a célula X representará a coordenada  *x*  do primeiro vértice de uma forma.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="5a4b9-110">Se a **linha MoveTo** aparecer entre duas linhas, a célula X representará a coordenada x do primeiro  *vértice*  após a quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="5a4b9-111">Y</span><span class="sxs-lookup"><span data-stu-id="5a4b9-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="5a4b9-112">Se a **linha MoveTo** for a primeira linha da seção, a célula Y representará a coordenada  *y*  do primeiro vértice de uma forma.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="5a4b9-113">Se a **linha MoveTo** aparecer entre duas linhas, a célula Y representará a coordenada  *y*  do primeiro vértice após a quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a4b9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a4b9-114">Remarks</span></span>

<span data-ttu-id="5a4b9-115">A **linha MoveTo** conterá as coordenadas  *x*  e  *y*  do primeiro vértice da forma se a linha **MoveTo** for a primeira linha da seção.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="5a4b9-116">Normalmente, esse é o primeiro vértice inserido quando a forma foi desenhada e não necessariamente corresponde ao ponto inicial de uma forma 1D.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="5a4b9-117">Uma seção geometry deve começar com uma **linha RelMoveTo** ou **MoveTo,** mas você também pode usar as linhas **MoveTo** e **RelMoveTo** para representar uma lacuna no aparamento do caminho de uma forma.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="5a4b9-118">No entanto, quando o caminho é usado para definir o limite de uma região preenchida, esse espaçamento é interpretado como um segmento de uma linha reta.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="5a4b9-119">Para inserir tal lacuna, insira uma linha entre duas linhas e altere o tipo de linha para **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="5a4b9-120">Se a **linha MoveTo** estiver entre duas linhas, ela conterá as coordenadas  *x*  e  *y*  do primeiro vértice da linha após a quebra no caminho da forma.</span><span class="sxs-lookup"><span data-stu-id="5a4b9-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

