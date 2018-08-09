---
title: Linha EllipticalArcTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contém x e y-coordenadas do ponto de extremidade de um arco elíptico, x e y-coordenadas dos pontos de controle do arco, ângulo de x-eixo ao eixo principal da elipse e a razão entre os eixos principal e secundária da elipse.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771794"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Linha EllipticalArcTo (Seção Geometry)

Contém *x* e *y* - coordenadas do ponto de extremidade do arco elíptico, *x* - e *y* -coordenadas dos pontos de controle do arco, ângulo do *x* -eixo ao eixo principal da elipse e proporção entre principal da elipse e secundária eixos r. 
  
Uma linha EllipticalArcTo contém as células a seguir.
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final em um arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final em um arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordenadas do ponto de controle do arco; um ponto do arco. O ponto de controle está localizado melhor sobre na metade entre exagerada vértices do arco. Caso contrário, o arco pode aumentar para um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -coordenadas do ponto de controle do arco.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |O ângulo do eixo de principal do arco em relação a *x* -o eixo de seu pai.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |
   

