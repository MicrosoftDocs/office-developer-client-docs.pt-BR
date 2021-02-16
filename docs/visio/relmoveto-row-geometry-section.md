---
title: Linha RelMoveTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contém as coordenadas x e y do primeiro vértice de uma forma ou do x - e y -coordenadas do primeiro vértice após uma quebra em um caminho, relativas à altura e largura da forma.
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414197"
---
# <a name="relmoveto-row-geometry-section"></a>Linha RelMoveTo (Seção Geometry)

Contém as coordenadas  *x*  e  *y*  do primeiro vértice de uma forma ou x  *-*  e  *y*  -coordenadas do primeiro vértice após uma quebra em um caminho, relativas à altura e largura da forma. 
  
> [!NOTE]
> Uma **linha RelMoveTo** só pode ser persistente nos formatos de arquivo .vsdx, .vsdm, .vstx, .vstm, .vssx e .vssm. Quando um arquivo é salvo nos formatos Visio 2003-2010, a linha **RelMoveTo** é convertida em uma [linha MoveTo.](moveto-row-geometry-section.md) 
  
Uma **linha RelMoveTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Se a **linha RelMoveTo** for a primeira linha da seção, a célula X representará a coordenada x do primeiro  *vértice*  de uma forma em relação à largura da forma. Se a **linha RelMoveTo** aparecer entre duas linhas, a célula X representará a coordenada x do primeiro  *vértice*  após a quebra no caminho.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Se a **linha RelMoveTo** for a primeira linha da seção, a célula Y representará a coordenada  *y*  do primeiro vértice de uma forma. Se a **linha RelMoveTo** aparecer entre duas linhas, a célula Y representará a coordenada  *y*  do primeiro vértice após a quebra no caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores na **linha RelMoveTo** são equivalentes aos valores em uma [linha MoveTo](moveto-row-geometry-section.md) que são multiplicados pela largura e altura da forma. Por exemplo: uma linha **RelMoveTo** onde o valor da célula **X** é "0" e o valor da célula **Y** é "0,5" poderia ser substituído pela linha **MoveTo** onde o valor da célula **X** é a fórmula "Width 0" e a célula Y é a *fórmula "Height* 0,5". 
  
A **linha RelMoveTo** conterá as coordenadas  *x*  e  *y*  do primeiro vértice da forma se a linha MoveTo for a primeira linha da seção. Normalmente, esse é o primeiro vértice inserido quando a forma foi desenhada e não necessariamente corresponde ao ponto inicial de uma forma 1D. 
  
Uma seção **Geometry** deve começar com uma linha **MoveTo** ou **RelMoveTo,** mas você também pode usar a linha **RelMoveTo** e a linha **MoveTo** para representar uma lacuna no aparamento do caminho de uma forma em relação à largura e altura da forma. No entanto, quando o caminho é usado para definir o limite de uma região preenchida, esse espaçamento é interpretado como um segmento de uma linha reta. Para inserir tal lacuna, insira uma linha entre duas linhas e altere o tipo de linha para **RelMoveTo**. Se a **linha RelMoveTo** estiver entre duas linhas, ela conterá as coordenadas  *x*  e  *y*  do primeiro vértice da linha após a quebra no caminho da forma. 
  

