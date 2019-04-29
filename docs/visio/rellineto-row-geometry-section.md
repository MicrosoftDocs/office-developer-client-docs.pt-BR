---
title: Linha RelLineTo (seção geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contém as coordenadas x e y do vértice final de um segmento de linha reta em relação à largura e à altura de uma forma.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437158"
---
# <a name="rellineto-row-geometry-section"></a>Linha RelLineTo (seção geometry)

Contém as coordenadas *x* e *y* do vértice final de um segmento de linha reta em relação à largura e à altura de uma forma. 
  
> [!NOTE]
> Uma linha **RelLineTo** só pode persistir nos formatos de arquivo. vsdx,. vsdm,. vstx,. VSTM,. vssx e. vssm. Quando um arquivo é salvo nos formatos do Visio 2003-2010, a linha **RelLineTo** é convertida em uma linha [LineTo](lineto-row-geometry-section.md) . 
  
Uma linha **RelLineTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do vértice final de um segmento de linha reta em relação à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do vértice final de um segmento de linha reta em relação à altura da forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores na linha **RelLineTo** são equivalentes a valores em uma linha [LineTo](lineto-row-geometry-section.md) que são multiplicados pela largura e altura da forma. Por exemplo: uma linha **RelLineTo** em que o valor da célula **X** é "0" e o valor da célula **Y** é "0,5" pode ser substituído pela linha **LineTo** onde o valor da célula **X** é a fórmula "largura*0" e a célula **Y** é o fórmula "altura*0,5". 
  

