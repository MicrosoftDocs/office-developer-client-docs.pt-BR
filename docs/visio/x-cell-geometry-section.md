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
description: Representa um x-coordenadas em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773298"
---
# <a name="x-cell-geometry-section"></a>Célula X (Seção Geometry)

Representa um *x* -coordenadas em uma forma em coordenadas locais. Esta tabela descreve a célula X com base na linha na qual está localizada. 
  
|**Row**|**Descrição**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Se a linha MoveTo for a primeira linha na seção, a célula X representará a *x* -coordenadas do primeiro vértice de um caminho. Se a linha MoveTo aparecer entre duas linhas, a célula X representará a *x* -coordenadas do primeiro vértice depois da quebra no caminho.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | *X* -coordenadas do vértice final de um segmento de linha reta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *X* -coordenadas do vértice final de um arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X* -coordenadas do vértice final de um arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *X* -coordenadas do vértice final de uma polilinha.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | *X* -coordenadas do último ponto de controle de uma B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | *X* -coordenadas do segundo ponto de controle de uma spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *X* -coordenadas de um ponto de controle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Um *x* -coordenadas de um ponto em uma linha infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | *X* -coordenadas do centro da elipse.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula X pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . X *j* onde *i* e *j* = < 1 >, 2, 3...  <br/> |
|| Geometria *i* . X1 (linhas InfiniteLine e Ellipse) onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula X pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Linhas InfiniteLine e Ellipse)  <br/> |
| Índice da célula:  <br/> |**visX** (Linhas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, PolylineTo, SplineStart e SplineKnot)  <br/> |
||**visInfiniteLineX1** (Linha InfiniteLine)  <br/> |
||**visEllipseCenterX** (Linha ellipse)  <br/> |
   

