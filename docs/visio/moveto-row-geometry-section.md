---
title: Linha MoveTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contém os x e y - coordenadas do primeiro vértice de uma forma ou representa x - e y-coordenadas do primeiro vértice depois de uma quebra no caminho.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772401"
---
# <a name="moveto-row-geometry-section"></a>Linha MoveTo (Seção Geometry)

Contém os *x* e *y* - coordenadas do primeiro vértice de uma forma ou representa o *x* - e *y* -coordenadas do primeiro vértice depois de uma quebra no caminho. 
  
Uma linha **MoveTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Se a linha **MoveTo** for a primeira linha na seção, a célula X representará a *x* -coordenadas do primeiro vértice de uma forma. Se a linha **MoveTo** aparecer entre duas linhas, a célula X representará a *x* -coordenadas do primeiro vértice depois da quebra no caminho.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Se a linha **MoveTo** for a primeira linha na seção, a célula Y representará a *y* -coordenadas do primeiro vértice de uma forma. Se a linha **MoveTo** aparecer entre duas linhas, a célula Y representará a *y* -coordenadas do primeiro vértice depois da quebra no caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

A linha **MoveTo** contém os *x* e *y* -coordenadas do primeiro vértice da forma se a linha **MoveTo** for a primeira linha na seção. Normalmente, esse é o primeiro vértice inserido quando a forma foi desenhada e não correspondem necessariamente ao ponto inicial de uma forma 1D. 
  
Uma seção geometry deve começar com uma **RelMoveTo** ou uma linha **MoveTo** , mas você também pode usar as linhas **MoveTo** e **RelMoveTo** para representar um espaçamento na pincelada do caminho de uma forma. No entanto, quando o caminho é usado para definir o limite de uma região preenchida, esse espaçamento é interpretado como um segmento de linha reta. Para inserir tal espaçamento, insira uma linha entre duas linhas e altere o tipo de linha para **MoveTo**. Se a linha **MoveTo** for entre duas linhas, que contém o *x* e *y* -coordenadas do primeiro vértice da linha depois da quebra no caminho da forma. 
  

