---
title: Célula A (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula A com base na linha na qual está localizada.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541299"
---
# <a name="a-cell-geometry-section"></a>Célula A (Seção Geometry)

Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula A com base na linha na qual está localizada.
  
|Linha|Descrição|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | A distância do ponto médio de um arco até o ponto médio de sua corda.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | A  *coordenada x*  do ponto de controle do arco, um ponto no arco. O ponto de controle é melhor localizado aproximadamente no meio dos vértices inicial e final do arco. Caso contrário, o arco pode aumentar até um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | A fórmula da polilinha.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | O penúltimo nó da B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | O segundo nó da spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Um dos nós da spline (exceto o último ou os dois primeiros).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Uma *coordenada x* de um ponto na linha infinita; emparelhado com uma coordenada *y* representada pela [célula B.](b-cell-geometry-section.md)  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Uma *coordenada x* de um ponto na elipse; emparelhado com uma coordenada *y* representada pela [célula B.](b-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula A pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry  *i*  . A  *j*            onde  *i e*  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . A1 (linhas InfiniteLine e Ellipse) onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de linha:  <br/> |**visRowVertex**  +   *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex**(linhas Ellipse e InfiniteLine)  <br/> |
| Índice da célula:  <br/> |**visBow**(linha ArcTo)  <br/> |
||**visControlX** (EllipticalArcTo row)  <br/> |
||**visControlY** (linha EllipticalArcTo)  <br/> |
||**visPolylineData** (linha Polyline)  <br/> |
||**visNURBSKnot** (linha NURBSTo)  <br/> |
||**visSplineKnot** (linhas SplineStart e SplineKnot)  <br/> |
||**visInfiniteLineX2** (linha InfiniteLine)  <br/> |
||**visEllipseMajorX** (linha Ellipse)  <br/> |
   

