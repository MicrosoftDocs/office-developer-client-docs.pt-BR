---
title: Célula ReplaceCopyCells (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica uma lista das células na ShapeSheet que são copiadas de uma forma antiga à forma de substituição durante uma operação de substituição de forma.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772681"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Célula ReplaceCopyCells (Seção Change Shape Behavior)

Indica uma lista das células na ShapeSheet que são copiadas de uma forma antiga à forma de substituição durante uma operação de substituição de forma. 
  
## <a name="remarks"></a>Comentários

A forma mestra da substituição deve conter uma chamada de função **DEPENDSON** na célula **ReplaceCopyCells** , onde cada argumento na função for uma referência a uma célula. Essas células são copiadas da forma antiga à forma resultante de uma operação de substituição de forma, independentemente de onde eles estão localizados no ShapeSheet. 
  
Valores e/ou em fórmulas que fazem referência a outras células são copiadas para a forma resultante. Se a forma resultante não tiver a célula referenciada, a célula copiada contém somente o valor. 
  
Referências na célula **ReplaceCopyCells** substituem o conjunto de proteção em células, conforme definido na seção de **proteção** e a **ReplaceLockFormat**, **ReplaceLockShapeData**e **ReplaceLockText** células. 
  
Para fazer referência à célula **ReplaceCopyCells** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceCopyCells  <br/> |
   
Para obter uma referência à célula **ReplaceCopyCells** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceCopyCells** <br/> |
   

