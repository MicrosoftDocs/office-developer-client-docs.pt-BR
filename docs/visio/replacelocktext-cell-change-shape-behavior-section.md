---
title: Célula ReplaceLockText (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. O ReplaceLockText determina se o texto exibido no mestre substitui o texto da forma que está sendo substituído.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772727"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Célula ReplaceLockText (Seção Change Shape Behavior)

Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. O **ReplaceLockText** determina se o texto exibido no mestre substitui o texto da forma que está sendo substituído. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> | O texto na forma mestra substitui o texto na forma antigo. Além disso, a forma mestra substitui os valores das células nas seções a seguir durante uma operação de substituição de forma:  <br/> Seção **Text Fields**  <br/> Seção **Text Block Format**  <br/> |
|FALSO  <br/> |A forma de substituição contém qualquer texto, campos de texto ou outras propriedades de texto da forma antiga que foram adicionadas à forma.  <br/> Quando a forma de substituição contém propriedades de texto da forma antiga, a forma de substituição tem também os valores das seções de **parágrafo** e **caractere** da forma antiga, caso possuam mais de uma linha.  <br/> |
   
Se definido como verdadeiro (1), os valores da forma mestra substitui os valores das seguintes opções na forma sendo substituída:
  
- [Célula TheText (Seção Events)](thetext-cell-events-section.md)
    
- Células na [seção Character](character-section.md)
    
- Células na [seção Paragraph](paragraph-section.md)
    
- Células na [seção Tabs](tabs-section.md)
    
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ReplaceLockText** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockText  <br/> |
   
Para obter uma referência à célula **ReplaceLockText** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceLockText** <br/> |
   

