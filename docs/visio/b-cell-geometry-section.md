---
title: Célula B (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula B com base na linha na qual está localizada.
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537791"
---
# <a name="b-cell-geometry-section"></a>Célula B (Seção Geometry)

Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula B com base na linha na qual está localizada.
  
|Linha|Descrição|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | A  *coordenada y*  do ponto de controle de um arco.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | A última espessura da B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | O primeiro nó de uma spline.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Uma *coordenada y* de um ponto em uma linha infinita; emparelhado com uma coordenada *x* representada pela [célula A.](a-cell-geometry-section.md)  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Uma *coordenada y* de um ponto em uma elipse; emparelhado com uma coordenada *x* representada pela [célula A.](a-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula B pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry  *i*  . B  *j*            onde  *i*  e  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . B1 (Linhas InfiniteLine e Ellipse)  <br/> |
   
Para fazer referência à célula B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de linha:  <br/> |**visRowVertex**  +   *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex**(linhas Ellipse e InfiniteLine)  <br/> |
| Índice da célula:  <br/> |**visControlX** (EllipticalArcTo row)  <br/> |
||**visControlY** (linha EllipticalArcTo)  <br/> |
||**visNURBSWeight**(linha NURBSTo)  <br/> |
||**visSplineKnot2**(linha SplineStart)  <br/> |
||**visInfiniteLineY2**(linha InfiniteLine)  <br/> |
||**visEllipseMajorY**(linha Ellipse)  <br/> |
   

