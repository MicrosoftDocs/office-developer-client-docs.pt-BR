---
title: Linha RelMoveTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contém os x e y - coordenadas do primeiro vértice de uma forma ou o x - e y-coordenadas do primeiro vértice depois de uma quebra no caminho, em relação a altura e largura da forma.
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772690"
---
# <a name="relmoveto-row-geometry-section"></a>Linha RelMoveTo (Seção Geometry)

Contém os *x* e *y* - coordenadas do primeiro vértice de uma forma ou o *x* - e *y* -coordenadas do primeiro vértice depois de uma quebra no caminho, em relação a altura e largura da forma. 
  
> [!NOTE]
> Uma linha **RelMoveTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm. Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelMoveTo** é convertida em uma linha [MoveTo](moveto-row-geometry-section.md) . 
  
Uma linha de **RelMoveTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Se a linha **RelMoveTo** for a primeira linha na seção, a célula X representará a *x* -coordenadas do primeiro vértice de uma forma relativa à largura da forma. Se a linha de **RelMoveTo** aparecer entre duas linhas, a célula X representará a *x* -coordenadas do primeiro vértice depois da quebra no caminho.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Se a linha **RelMoveTo** for a primeira linha na seção, a célula Y representará a *y* -coordenadas do primeiro vértice de uma forma. Se a linha de **RelMoveTo** aparecer entre duas linhas, a célula Y representará a *y* -coordenadas do primeiro vértice depois da quebra no caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Valores na linha **RelMoveTo** são equivalentes aos valores em uma linha [MoveTo](moveto-row-geometry-section.md) que serão multiplicados pela largura e altura da forma. Por exemplo: uma linha **RelMoveTo** onde o valor da célula **X** é "0" e o valor da célula **Y** é "0,5" poderia ser substituída pela linha **MoveTo** onde o valor da célula **X** é a fórmula "largura*0" e a célula **Y** é o fórmula "altura*0.5." 
  
A linha **RelMoveTo** contém os *x* e *y* -coordenadas do primeiro vértice da forma se a linha MoveTo for a primeira linha na seção. Normalmente, esse é o primeiro vértice inserido quando a forma foi desenhada e não correspondem necessariamente ao ponto inicial de uma forma 1D. 
  
Uma seção **Geometry** deve começar com um **MoveTo** ou uma linha **RelMoveTo** , mas você também pode usar a linha de **RelMoveTo** e a linha **MoveTo** para representar um espaçamento na pincelada do caminho de uma forma em relação à largura e a altura da forma. No entanto, quando o caminho é usado para definir o limite de uma região preenchida, esse espaçamento é interpretado como um segmento de linha reta. Para inserir tal espaçamento, insira uma linha entre duas linhas e altere o tipo de linha para **RelMoveTo**. Se a linha **RelMoveTo** for entre duas linhas, que contém o *x* e *y* -coordenadas do primeiro vértice da linha depois da quebra no caminho da forma. 
  

