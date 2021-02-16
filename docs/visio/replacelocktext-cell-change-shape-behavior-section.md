---
title: Célula ReplaceLockText (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica se os valores das células especificadas em uma forma mestra substituem os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. ReplaceLockText determina se o texto exibido no Mestre substitui o texto da forma que está sendo substituída.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411915"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Célula ReplaceLockText (Seção Change Shape Behavior)

Indica se os valores das células especificadas em uma forma mestra substituem os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. **ReplaceLockText** determina se o texto exibido no Mestre substitui o texto da forma que está sendo substituída. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> | O texto na forma mestra substitui o texto na forma antiga. Além disso, a forma mestra substitui os valores das células nas seções a seguir durante uma operação de substituição de forma:  <br/> **Seção Text Fields**  <br/> **Seção Text Block Format**  <br/> |
|FALSE  <br/> |A forma de substituição contém qualquer texto, campos de texto ou outras propriedades de texto da forma antiga que foram adicionadas à forma.  <br/> Quando a forma de substituição contém propriedades de texto da forma antiga, a forma de substituição também tem os valores das seções **Character** e **Paragraph** da forma antiga se elas têm mais de uma linha.  <br/> |
   
Se definido como VERDADEIRO (1), os valores da forma Mestre substituirão os valores do seguinte na forma que está sendo substituída:
  
- [Célula TheText (Seção Events)](thetext-cell-events-section.md)
    
- Células na seção [Character](character-section.md)
    
- Células na [seção Paragraph](paragraph-section.md)
    
- Células na [seção Tabs](tabs-section.md)
    
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ReplaceLockText** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockText  <br/> |
   
Para fazer referência à célula **ReplaceLockText** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de célula:  <br/> |**visReplaceLockText** <br/> |
   

