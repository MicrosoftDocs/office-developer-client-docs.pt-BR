---
title: Linha RelEllipticalArcTo (seção geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contém as coordenadas x e y de um ponto de extremidade de um arco elíptico em relação à largura e altura da forma, as coordenadas x e y dos pontos de controle no arco em relação à largura e altura da forma, ângulo do eixo x para o eixo principal da elipse e a proporção entre t eixos principais e secundários de sua elipse.
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409094"
---
# <a name="relellipticalarcto-row-geometry-section"></a>Linha RelEllipticalArcTo (seção geometry)

Contém as coordenadas *x* e *y* do ponto de extremidade de um arco elíptico em relação à largura e altura da forma, coordenadas *x* e *y* dos pontos de controle no arco em relação à largura e altura da forma, ângulo do eixo *x*   -eixo do eixo principal da elipse e a proporção entre os eixos principal e secundário da elipse. 
  
> [!NOTE]
> Uma linha **RelEllipticalArcTo** só pode persistir nos formatos de arquivo. vsdx,. vsdm,. vstx,. VSTM,. vssx e. vssm. Quando um arquivo é salvo nos formatos do Visio 2003-2010, a linha **RelEllipticalArcTo** é convertida em uma linha [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) . 
  
Uma linha **RelEllipticalArcTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do vértice final em um arco em relação à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do vértice final em um arco em relação à altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A coordenada *x* do ponto de controle do arco em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado sobre a metade entre os vértices inicial e final do arco. Caso contrário, o arco pode chegar a um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |
|[A.b.c.](b-cell-geometry-section.md) <br/> |A coordenada *y* do ponto de controle de um arco em relação à largura da forma.  <br/> |
|[Unidade](c-cell-geometry-section.md) <br/> |O ângulo do eixo principal do arco em relação ao eixo *x* de seu pai.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores na linha **RelEllipticalArcTo** são equivalentes a valores em uma linha [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) , multiplicados pela largura e altura da forma. por exemplo: uma linha **RelEllipticalArcTo** onde as **células X**, **Y**, **a**, **B**, **C**e **D** têm os valores 1, 1, 1,5, 0,5, 15 graus e 1,5 (respectivamente) podem ser substituídos por uma linha **EllipticalArcTo** com as fórmulas `Width*1`de `Height*1'`célula `Width*1.5`, `Height*0.5`,,, 15 graus, e 1,5 (respectivamente).
  

