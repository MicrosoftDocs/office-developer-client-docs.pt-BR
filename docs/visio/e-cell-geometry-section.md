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
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423563"
---
# <a name="e-cell-geometry-section"></a>Célula E (Seção Geometry)

Contém uma fórmula de B-spline racional não-uniforme (NURBS).
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula E pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry *i* . E *j* onde *i* e *j* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula E pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de linha:  <br/> |**visRowVertex** +  *j* onde *j* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visNURBSData** <br/> |
   

