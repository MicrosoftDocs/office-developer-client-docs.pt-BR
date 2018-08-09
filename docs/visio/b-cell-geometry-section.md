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
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771290"
---
# <a name="b-cell-geometry-section"></a>Célula B (Seção Geometry)

Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula B com base na linha na qual está localizada.
  
|**Row**|**Descrição**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Y* -coordenadas do ponto de controle do arco.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | A última espessura da B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | O primeiro nó de uma spline.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Um *y* -coordenadas de um ponto em uma linha infinita; juntamente com *x* -coordenada representada pela célula [A](a-cell-geometry-section.md) .  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Um *y* -coordenadas de um ponto em um elipse, juntamente com *x* -coordenada representada pela célula [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula B pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . B *j* onde *i* e *j* = < 1 >, 2, 3...  <br/> |
|| Geometria *i* . B1 (linhas InfiniteLine e Ellipse)  <br/> |
   
Para fazer referência à célula B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex **(linhas Ellipse e InfiniteLine)  <br/> |
| Índice da célula:  <br/> |**visControlX** (EllipticalArcTo row)  <br/> |
||**visControlY** (linha EllipticalArcTo)  <br/> |
||**visNURBSWeight **(linha NURBSTo)  <br/> |
||**visSplineKnot2 **(linha SplineStart)  <br/> |
||**visInfiniteLineY2 **(linha InfiniteLine)  <br/> |
||**visEllipseMajorY **(linha Ellipse)  <br/> |
   

