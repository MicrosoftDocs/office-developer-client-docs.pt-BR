---
title: Linha PolylineTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Contém x e y-coordenadas do último ponto de uma polilinha e uma fórmula de polilinha.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772503"
---
# <a name="polylineto-row-geometry-section"></a>Linha PolylineTo (Seção Geometry)

Contém *x* e *y* -coordenadas do último ponto de uma polilinha e uma fórmula de polilinha. 
  
Uma linha PolylineTo contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final de uma polilinha.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final de uma polilinha.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A fórmula da polilinha.  <br/> |
   
## <a name="remarks"></a>Comentários

Linhas representadas como uma linha PolylineTo são equivalentes a linhas representadas como uma sequência de linhas LineTo, mas uma linha PolylineTo é mais eficiente. Você pode alterar uma linha PolylineTo para uma linha LineTo de forma que seja possível ver a geometria da forma facilmente. Para fazer isso, clique com o botão direito do mouse na linha PolylineTo e clique em **Expandir Linha** no menu de atalho. 
  
Para alterar um tipo de linha para uma linha PolylineTo, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho. 
  

