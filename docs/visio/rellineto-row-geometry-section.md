---
title: Linha RelLineTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contém x - e y-coordenadas do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772679"
---
# <a name="rellineto-row-geometry-section"></a>Linha RelLineTo (Seção Geometry)

Contém *x* - e *y* -coordenadas do vértice final de um segmento de linha reta em relação à largura e altura de uma forma. 
  
> [!NOTE]
> Uma linha **RelLineTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm. Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelLineTo** é convertida em uma linha [LineTo](lineto-row-geometry-section.md) . 
  
Uma linha de **RelLineTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final de um segmento de linha reta em relação à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final de um segmento de linha reta em relação à altura da forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Valores na linha **RelLineTo** são equivalentes aos valores em uma linha [LineTo](lineto-row-geometry-section.md) que serão multiplicados pela largura e altura da forma. Por exemplo: uma linha **RelLineTo** onde o valor da célula **X** é "0" e o valor da célula **Y** é "0,5" pode ser substituída por linha **LineTo** onde o valor da célula **X** é a fórmula "largura*0" e a célula **Y** é o fórmula "altura*0.5." 
  

