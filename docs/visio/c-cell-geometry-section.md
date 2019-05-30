---
title: Célula C (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula C com base na linha na qual está localizada.
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541887"
---
# <a name="c-cell-geometry-section"></a>Célula C (Seção Geometry)

Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula C com base na linha na qual está localizada.
  
|Linha|Descrição|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | O ângulo do eixo principal do arco em relação ao eixo *x* de seu pai.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | O primeiro nó da B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | O último nó de uma spline.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Uma coordenada *x* de um ponto em uma elipse; emparelhado com a coordenada *y* representada pela célula [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula C pelo nome a partir de outra fórmula ou de um programa que usa a **** propriedade Cells, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry *i* . C *j* onde *i* e *j* = <1>, 2, 3...  <br/> |
|| Geometry *i* . C1 (linha Ellipse)  <br/> |
   
Para obter uma referência para a célula C pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex **(linha Ellipse)  <br/> |
| Índice de célula:  <br/> |**visEccentricityAngle** (Linha EllipticalArcTo)  <br/> |
||**visNURBSKnotPrev** (Linha NURBSto)  <br/> |
||**visSplineKnot3** (Linha SplineStart)  <br/> |
||**visEllipseMinorX** (Linha Ellipse)  <br/> |
   

