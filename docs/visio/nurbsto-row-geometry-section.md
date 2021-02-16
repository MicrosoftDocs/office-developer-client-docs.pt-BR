---
title: Linha NURBSTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251758
localization_priority: Normal
ms.assetid: 7e47acfe-5ec0-3689-eb89-0168f596a739
description: Contém as coordenadas x e y, a posição do segundo ao último nó, a posição da última peso, a posição do primeiro nó, a posição da primeira peso e a fórmula para uma B-spline racional não uniforme (NURBS).
ms.openlocfilehash: a5fc83f9581277580d076c2a850bfe937602aef0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404712"
---
# <a name="nurbsto-row-geometry-section"></a>Linha NURBSTo (Seção Geometry)

Contém as coordenadas  *x*  e  *y,*  a posição do segundo ao último nó, a posição da última peso, a posição do primeiro nó, a posição da primeira peso e a fórmula para uma B-spline racional não uniforme (NURBS). 
  
Uma linha NURBSTo contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A  *coordenada x*  do último ponto de controle de uma NURBS.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A  *coordenada y*  do último ponto de controle de uma NURBS.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |O penúltimo nó de uma NURBS.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |A última espessura de uma NURBS.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |O primeiro nó de uma NURBS.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A primeira espessura de uma NURBS.  <br/> |
|[E](e-cell-geometry-section.md) <br/> |Uma fórmula NURBS.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma NURBS é um meio comum de representar matematicamente uma curva. Crie uma NURBS com a ferramenta **Forma Livre**. 
  

