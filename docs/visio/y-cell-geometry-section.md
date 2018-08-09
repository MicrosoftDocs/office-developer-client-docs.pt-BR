---
title: Célula Y (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Representa um y-coordenadas em uma forma em coordenadas locais. Esta tabela descreve a célula Y com base na linha na qual está localizada.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773333"
---
# <a name="y-cell-geometry-section"></a>Célula Y (Seção Geometry)

Representa um *y* -coordenadas em uma forma em coordenadas locais. Esta tabela descreve a célula Y com base na linha na qual está localizada. 
  
|**Row**|**Descrição**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Se a linha MoveTo for a primeira linha na seção, a célula Y representará a *y* -coordenadas do primeiro vértice de um caminho. Se a linha MoveTo aparecer entre duas linhas, a célula Y representará a *y* -coordenadas do primeiro vértice depois da quebra no caminho.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | *Y* -coordenadas do vértice final de um segmento de linha reta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *Y* -coordenadas do vértice final de um arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Y* -coordenadas do vértice final de um arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *Y* -coordenadas do vértice final de uma polilinha.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | *Y* -coordenadas do último ponto de controle de uma B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | *Y* -coordenadas do segundo ponto de controle de uma spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *Y* -coordenadas de um ponto de controle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Y -* coordenadas de um ponto em uma linha infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | *Y* -coordenadas do centro da elipse.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . Y *j* onde *i* e *j* = < 1 >, 2, 3...  <br/> |
|| Geometria *i* . Y1 (linhas InfiniteLine e Ellipse) onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex **(linhas Ellipse e InfiniteLine)  <br/> |
| Índice da célula:  <br/> |**visY **(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)  <br/> |
||**visInfiniteLineY1 **(linha InfiniteLine)  <br/> |
||**visEllipseCenterY **(linha Ellipse)  <br/> |
   

