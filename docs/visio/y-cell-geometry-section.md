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
description: Representa uma coordenada y em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540487"
---
# <a name="y-cell-geometry-section"></a>Célula Y (Seção Geometry)

Representa uma coordenada  *y*  em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada. 
  
|Linha|Descrição|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Se a linha MoveTo for a primeira linha da seção, a célula Y representará a coordenada  *y*  do primeiro vértice de um caminho. Se a linha MoveTo aparecer entre duas linhas, a célula Y representará a coordenada  *y*  do primeiro vértice após a quebra no caminho.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | A  *coordenada y*  do vértice final de um segmento de linha reta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | A  *coordenada y*  do vértice final de um arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | A  *coordenada y*  do vértice final de um arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | A  *coordenada y*  do vértice final de uma polilinha.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | A  *coordenada y*  do último ponto de controle de uma B-spline racional não uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | A  *coordenada y*  do segundo ponto de controle de uma spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | A  *coordenada y*  de um ponto de controle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Uma  *coordenada y*  de um ponto na linha infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | A  *coordenada y*  do centro da elipse.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry  *i*  . Y  *j*            onde  *i*  e  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . Y1 (linhas InfiniteLine e Ellipse) onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de linha:  <br/> |**visRowVertex**  +   *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex**(linhas Ellipse e InfiniteLine)  <br/> |
| Índice da célula:  <br/> |**visY**(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)  <br/> |
||**visInfiniteLineY1**(linha InfiniteLine)  <br/> |
||**visEllipseCenterY**(linha Ellipse)  <br/> |
   

