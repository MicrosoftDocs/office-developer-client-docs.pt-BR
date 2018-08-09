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
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771438"
---
# <a name="c-cell-geometry-section"></a>Célula C (Seção Geometry)

Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula C com base na linha na qual está localizada.
  
|**Row**|**Descrição**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | O ângulo do eixo de principal do arco em relação a *x* -o eixo de seu pai.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | O primeiro nó da B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | O último nó de uma spline.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Um *x* -coordenadas de um ponto em um elipse, juntamente com o *y* -coordenada representada pela célula [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula C pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . C *j* onde *i* e *j* = < 1 >, 2, 3...  <br/> |
|| Geometria *i* . C1 (linha Ellipse)  <br/> |
   
Para fazer referência à célula C pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex **(linha Ellipse)  <br/> |
| Índice da célula:  <br/> |**visEccentricityAngle **(linha EllipticalArcTo)  <br/> |
||**visNURBSKnotPrev **(linha NURBSTo)  <br/> |
||**visSplineKnot3 **(linha SplineStart)  <br/> |
||**visEllipseMinorX **(linha Ellipse)  <br/> |
   

