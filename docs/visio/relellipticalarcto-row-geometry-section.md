---
title: Linha RelEllipticalArcTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contém x e y - coordenadas do ponto de extremidade do arco elíptico em relação à largura da forma e a altura, x - e y-ângulo de coordenadas dos pontos de controle do arco em relação à largura e a altura da forma no x-eixo ao eixo principal da elipse e a razão entre t eixos da elipse s principais e secundárias.
ms.openlocfilehash: 417a2a92bc5c94f9620c7c6f1081ba81d93aa890
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772677"
---
# <a name="relellipticalarcto-row-geometry-section"></a>Linha RelEllipticalArcTo (Seção Geometry)

Contém *x* e *y* - coordenadas do ponto de extremidade do arco elíptico em relação à largura da forma e a altura, *x* - e *y* -ângulo de coordenadas dos pontos de controle do arco em relação à largura e a altura da forma dos *x*   -eixo ao eixo principal da elipse e a razão entre os eixos principal e secundária da elipse. 
  
> [!NOTE]
> Uma linha **RelEllipticalArcTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm. Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelEllipticalArcTo** é convertida em uma linha [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) . 
  
Uma linha de **RelEllipticalArcTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final em um arco relativa à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final em um arco em relação a altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordenadas do ponto de controle do arco em relação à largura da forma; um ponto do arco. O ponto de controle está localizado melhor sobre na metade entre exagerada vértices do arco. Caso contrário, o arco pode aumentar para um tamanho extremo para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -coordenadas do ponto de controle do arco em relação à largura da forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |O ângulo do eixo de principal do arco em relação a *x* -o eixo de seu pai.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |
   
## <a name="remarks"></a>Comentários

Valores na linha **RelEllipticalArcTo** são equivalentes aos valores em uma linha [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) , multiplicado pela largura e altura da forma. Por exemplo: um **RelEllipticalArcTo** linha onde as células **X**, **Y**, **A**, **B**, **C**e **D** têm os valores 1, 1, 1,5, 0,5, 15 graus e 1,5 (respectivamente) podem ser substituídos por uma linha **EllipticalArcTo** com as fórmulas de célula `Width*1`, `Height*1'`, `Width*1.5`, `Height*0.5`, 15 graus e 1,5 (respectivamente).
  

