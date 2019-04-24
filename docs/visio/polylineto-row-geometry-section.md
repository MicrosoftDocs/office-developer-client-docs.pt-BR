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
description: Contém as coordenadas x e y do último ponto de uma polilinha e uma fórmula de polilinha.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359826"
---
# <a name="polylineto-row-geometry-section"></a>Linha PolylineTo (Seção Geometry)

Contém as coordenadas *x* e *y* do último ponto de uma polilinha e uma fórmula de polilinha. 
  
Uma linha PolylineTo contém as células a seguir.
  
|**Cell**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do vértice final de uma polilinha.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do vértice final de uma polilinha.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A fórmula da polilinha.  <br/> |
   
## <a name="remarks"></a>Comentários

Linhas representadas como uma linha PolylineTo são equivalentes a linhas representadas como uma sequência de linhas LineTo, mas uma linha PolylineTo é mais eficiente. Você pode alterar uma linha PolylineTo para uma linha LineTo de forma que seja possível ver a geometria da forma facilmente. Para fazer isso, clique com o botão direito do mouse na linha PolylineTo e clique em **Expandir Linha** no menu de atalho. 
  
Para alterar um tipo de linha para uma linha PolylineTo, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho. 
  

