---
title: Linha ArcTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Contém as coordenadas x e y e a curva de um arco circular.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341402"
---
# <a name="arcto-row-geometry-section"></a>Linha ArcTo (Seção Geometry)

Contém as coordenadas *x* e *y* e a curva de um arco circular. 
  
Uma linha ArcTo contém as células a seguir.
  
|**Cell**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do vértice final de um arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do vértice final de um arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A distância do ponto médio de um arco até o ponto médio de sua corda.  <br/> |
   
## <a name="remarks"></a>Comentários

Os arcos desenhados no Visio são elípticos, mesmo se baseados em um círculo. Por padrão, os arcos desenhados são representados por uma linha EllipticalArcTo em uma janela ShapeSheet. Para mostrar uma linha ArcTo em uma janela ShapeSheet, desenhe um arco e depois altere o tipo de linha EllipticalArcTo para uma linha ArcTo; na verdade, você está alterando um arco elíptico para um arco circular.
  
Para alterar um tipo de linha, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho. 
  

