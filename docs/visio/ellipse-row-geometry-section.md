---
title: Linha Ellipse (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contém as coordenadas x e y do ponto central da elipse e dois pontos na elipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345679"
---
# <a name="ellipse-row-geometry-section"></a>Linha Ellipse (Seção Geometry)

Contém as coordenadas *x* e *y* do ponto central da elipse e dois pontos na elipse. 
  
Uma linha Ellipse contém as células a seguir.
  
|**Cell**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do ponto central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do ponto central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A coordenada x de um ponto na elipse; emparelhado com a coordenada *y* representada pela célula B.  <br/> |
|[A.b.c.](b-cell-geometry-section.md) <br/> |A coordenada *y* de um ponto na elipse; emparelhado com a coordenada x representada pela célula a.  <br/> |
|[Unidade](c-cell-geometry-section.md) <br/> |A coordenada *x* de outro ponto na elipse; emparelhado com a coordenada *y* representada pela célula D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A coordenada *y* de outro ponto na elipse; emparelhado com a coordenada *y* representada pela célula C.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma seção Geometry que contém uma linha Ellipse ou InfiniteLine não deveria conter qualquer outra linha.
  

