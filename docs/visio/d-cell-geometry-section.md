---
title: Célula D (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula D com base na linha na qual está localizada.
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771632"
---
# <a name="d-cell-geometry-section"></a>Célula D (Seção Geometry)

Representa informações diferentes em linhas diferentes. Esta tabela descreve a célula D com base na linha na qual está localizada.
  
|**Row**|**Descrição**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | A primeira espessura da B-spline racional não-uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | O grau de uma spline (um inteiro de 1 a 25).  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Um *y* -coordenadas de um ponto em um elipse, juntamente com o *x* -coordenada representada pela célula [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula D pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . D *j* onde *i* e *j* = < 1 >, 2, 3...  <br/> |
|| Geometria *i* . D1 (linha Ellipse) onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula D pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
||**visRowVertex **(linha Ellipse)  <br/> |
| Índice da célula:  <br/> |**visAspectRatio **(linha EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev **(linha NURBSTo)  <br/> |
||**visSplineDegree **(linha SplineStart)  <br/> |
||**visEllipseMinorY **(linha Ellipse)  <br/> |
   

