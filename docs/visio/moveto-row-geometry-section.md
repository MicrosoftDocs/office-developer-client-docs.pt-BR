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
description: Contém os x e y - coordenadas do primeiro vértice de uma forma ou representa x - e y-coordenadas do primeiro vértice depois de uma quebra no caminho.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772401"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="3244d-103">Linha MoveTo (Seção Geometry)</span><span class="sxs-lookup"><span data-stu-id="3244d-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="3244d-104">Contém os *x* e *y* - coordenadas do primeiro vértice de uma forma ou representa o *x* - e *y* -coordenadas do primeiro vértice depois de uma quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="3244d-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="3244d-105">Uma linha **MoveTo** contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="3244d-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="3244d-106">**Célula**</span><span class="sxs-lookup"><span data-stu-id="3244d-106">**Cell**</span></span>|<span data-ttu-id="3244d-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3244d-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3244d-108">X</span><span class="sxs-lookup"><span data-stu-id="3244d-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3244d-109">Se a linha **MoveTo** for a primeira linha na seção, a célula X representará a *x* -coordenadas do primeiro vértice de uma forma.</span><span class="sxs-lookup"><span data-stu-id="3244d-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="3244d-110">Se a linha **MoveTo** aparecer entre duas linhas, a célula X representará a *x* -coordenadas do primeiro vértice depois da quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="3244d-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="3244d-111">Y</span><span class="sxs-lookup"><span data-stu-id="3244d-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3244d-112">Se a linha **MoveTo** for a primeira linha na seção, a célula Y representará a *y* -coordenadas do primeiro vértice de uma forma.</span><span class="sxs-lookup"><span data-stu-id="3244d-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="3244d-113">Se a linha **MoveTo** aparecer entre duas linhas, a célula Y representará a *y* -coordenadas do primeiro vértice depois da quebra no caminho.</span><span class="sxs-lookup"><span data-stu-id="3244d-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3244d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3244d-114">Remarks</span></span>

<span data-ttu-id="3244d-115">A linha **MoveTo** contém os *x* e *y* -coordenadas do primeiro vértice da forma se a linha **MoveTo** for a primeira linha na seção.</span><span class="sxs-lookup"><span data-stu-id="3244d-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="3244d-116">Normalmente, esse é o primeiro vértice inserido quando a forma foi desenhada e não correspondem necessariamente ao ponto inicial de uma forma 1D.</span><span class="sxs-lookup"><span data-stu-id="3244d-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="3244d-117">Uma seção geometry deve começar com uma **RelMoveTo** ou uma linha **MoveTo** , mas você também pode usar as linhas **MoveTo** e **RelMoveTo** para representar um espaçamento na pincelada do caminho de uma forma.</span><span class="sxs-lookup"><span data-stu-id="3244d-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="3244d-118">No entanto, quando o caminho é usado para definir o limite de uma região preenchida, esse espaçamento é interpretado como um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="3244d-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="3244d-119">Para inserir tal espaçamento, insira uma linha entre duas linhas e altere o tipo de linha para **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="3244d-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="3244d-120">Se a linha **MoveTo** for entre duas linhas, que contém o *x* e *y* -coordenadas do primeiro vértice da linha depois da quebra no caminho da forma.</span><span class="sxs-lookup"><span data-stu-id="3244d-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

