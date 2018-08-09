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
description: Contém os x e y-coordenadas do ponto central da elipse e dois pontos na elipse.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771792"
---
# <a name="ellipse-row-geometry-section"></a>Linha Ellipse (Seção Geometry)

Contém os *x* e *y* -coordenadas do ponto central da elipse e dois pontos na elipse. 
  
Uma linha Ellipse contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do ponto central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do ponto central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A coordenada x de um ponto na elipse, juntamente com *y* -coordenada representada pela célula B.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -coordenadas de um ponto na elipse, juntamente com a coordenada x representada pela célula.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -coordenadas de um outro ponto na elipse; juntamente com *y* -coordenada representada pela célula D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*Y* -coordenadas de um outro ponto na elipse; juntamente com *y* -coordenada representada pela célula C.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma seção Geometry que contém uma linha Ellipse ou InfiniteLine não deveria conter qualquer outra linha.
  

