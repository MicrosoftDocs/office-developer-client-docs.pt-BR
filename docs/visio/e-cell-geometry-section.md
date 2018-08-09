---
title: Célula E (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contém uma fórmula de B-spline racional não-uniforme (NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771787"
---
# <a name="e-cell-geometry-section"></a>Célula E (Seção Geometry)

Contém uma fórmula de B-spline racional não-uniforme (NURBS).
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula E pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . F *j* onde *i* e *j* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula E pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visNURBSData** <br/> |
   

