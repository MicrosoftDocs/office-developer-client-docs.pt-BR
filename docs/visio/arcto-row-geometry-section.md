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
description: Contém os x e y-coordenadas e curva de um arco circular.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771274"
---
# <a name="arcto-row-geometry-section"></a>Linha ArcTo (Seção Geometry)

Contém os *x* e *y* -coordenadas e curva de um arco circular. 
  
Uma linha ArcTo contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final de um arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final de um arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A distância do ponto médio de um arco até o ponto médio de sua corda.  <br/> |
   
## <a name="remarks"></a>Comentários

Os arcos desenhados no Visio são elípticos, mesmo se baseados em um círculo. Por padrão, os arcos desenhados são representados por uma linha EllipticalArcTo em uma janela ShapeSheet. Para mostrar uma linha ArcTo em uma janela ShapeSheet, desenhe um arco e depois altere o tipo de linha EllipticalArcTo para uma linha ArcTo; na verdade, você está alterando um arco elíptico para um arco circular.
  
Para alterar um tipo de linha, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho. 
  

