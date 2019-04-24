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
description: Contém as coordenadas x e y de um ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse e a proporção entre os eixos principal e secundário da elipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345672"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Linha EllipticalArcTo (Seção Geometry)

Contém as coordenadas *x* e *y* de um ponto de extremidade de um arco elíptico, as coordenadas *x* e *y* dos pontos de controle no arco, ângulo do eixo *x* para o eixo principal da elipse e a proporção entre o maior e o Mino da elipse. eixos r. 
  
Uma linha EllipticalArcTo contém as células a seguir.
  
|**Cell**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do vértice final em um arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do vértice final em um arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A coordenada *x* do ponto de controle do arco; um ponto no arco. O ponto de controle é melhor localizado sobre a metade entre os vértices inicial e final do arco. Caso contrário, o arco pode chegar a um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |
|[A.b.c.](b-cell-geometry-section.md) <br/> |A coordenada *y* do ponto de controle de um arco.  <br/> |
|[Unidade](c-cell-geometry-section.md) <br/> |O ângulo do eixo principal do arco em relação ao eixo *x* de seu pai.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |
   

