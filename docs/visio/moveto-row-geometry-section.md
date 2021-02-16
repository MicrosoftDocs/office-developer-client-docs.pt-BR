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
description: Contém as coordenadas x e y do primeiro vértice de uma forma ou representa as coordenadas x e y do primeiro vértice após uma quebra em um caminho.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429695"
---
# <a name="moveto-row-geometry-section"></a>Linha MoveTo (Seção Geometry)

Contém as coordenadas  *x*  e  *y*  do primeiro vértice de uma forma ou representa as coordenadas  *x*  e  *y*  do primeiro vértice após uma quebra em um caminho. 
  
Uma **linha MoveTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Se a **linha MoveTo** for a primeira linha da seção, a célula X representará a coordenada  *x*  do primeiro vértice de uma forma. Se a **linha MoveTo** aparecer entre duas linhas, a célula X representará a coordenada x do primeiro  *vértice*  após a quebra no caminho.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Se a **linha MoveTo** for a primeira linha da seção, a célula Y representará a coordenada  *y*  do primeiro vértice de uma forma. Se a **linha MoveTo** aparecer entre duas linhas, a célula Y representará a coordenada  *y*  do primeiro vértice após a quebra no caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

A **linha MoveTo** conterá as coordenadas  *x*  e  *y*  do primeiro vértice da forma se a linha **MoveTo** for a primeira linha da seção. Normalmente, esse é o primeiro vértice inserido quando a forma foi desenhada e não necessariamente corresponde ao ponto inicial de uma forma 1D. 
  
Uma seção geometry deve começar com uma **linha RelMoveTo** ou **MoveTo,** mas você também pode usar as linhas **MoveTo** e **RelMoveTo** para representar uma lacuna no aparamento do caminho de uma forma. No entanto, quando o caminho é usado para definir o limite de uma região preenchida, esse espaçamento é interpretado como um segmento de uma linha reta. Para inserir tal lacuna, insira uma linha entre duas linhas e altere o tipo de linha para **MoveTo**. Se a **linha MoveTo** estiver entre duas linhas, ela conterá as coordenadas  *x*  e  *y*  do primeiro vértice da linha após a quebra no caminho da forma. 
  

