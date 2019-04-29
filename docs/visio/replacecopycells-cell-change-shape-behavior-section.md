---
title: Célula ReplaceCopyCells (seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica uma lista de células no ShapeSheet que são copiadas de uma forma antiga para a forma de substituição durante uma operação de substituição de forma.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409339"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Célula ReplaceCopyCells (seção Change Shape Behavior)

Indica uma lista de células no ShapeSheet que são copiadas de uma forma antiga para a forma de substituição durante uma operação de substituição de forma. 
  
## <a name="remarks"></a>Comentários

A forma mestre da substituição deve conter uma chamada de função de **dependência** na célula **ReplaceCopyCells** , onde cada argumento na função é uma referência a uma célula. Essas células são copiadas da forma antiga para a forma que resulta de uma operação de substituição de forma, independentemente de onde elas estão no ShapeSheet. 
  
Os valores e/ou fórmulas que fazem referência a outras células são copiados para a forma resultante. Se a forma resultante não tiver a célula referenciada, a célula copiada conterá apenas o valor. 
  
Referências na proteção de substituição de célula **ReplaceCopyCells** definidas nas células, conforme definido na seção **proteção** e nas células **ReplaceLockFormat**, **ReplaceLockShapeData**e **ReplaceLockText** . 
  
Para obter uma referência para a célula **ReplaceCopyCells** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceCopyCells  <br/> |
   
Para obter uma referência para a célula **ReplaceCopyCells** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceCopyCells** <br/> |
   

