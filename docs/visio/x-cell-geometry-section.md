---
title: Célula X (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Representa uma coordenada x em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada.
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538211"
---
# <a name="x-cell-geometry-section"></a>Célula X (Seção Geometry)

Representa uma  *coordenada x*  em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada. 
  
|Linha|Descrição|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Se a linha MoveTo for a primeira linha da seção, a célula X representará a coordenada  *x*  do primeiro vértice de um caminho. Se a linha MoveTo aparecer entre duas linhas, a célula X representará a coordenada  *x*  do primeiro vértice após a quebra no caminho.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | A  *coordenada x*  do vértice final de um segmento de linha reta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | A  *coordenada x*  do vértice final de um arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | A  *coordenada x*  do vértice final de um arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | A  *coordenada x*  do vértice final de uma polilinha.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | A  *coordenada x*  do último ponto de controle de uma B-spline racional não uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | A  *coordenada x*  do segundo ponto de controle de uma spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | A  *coordenada x*  de um ponto de controle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Uma  *coordenada x*  de um ponto na linha infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | A  *coordenada x*  do centro da elipse.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry  *i*  . X  *j*            onde  *i*  e  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . X1 (linhas InfiniteLine e Ellipse) onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de linha:  <br/> |**visRowVertex**  +   *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex**(linhas Ellipse e InfiniteLine)  <br/> |
| Índice da célula:  <br/> |**visX**(linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)  <br/> |
||**visInfiniteLineX1**(linha InfiniteLine)  <br/> |
||**visEllipseCenterX**(linha Ellipse)  <br/> |
   

