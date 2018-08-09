---
title: Célula LangID (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Indica o idioma no qual o texto foi inserido.
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772143"
---
# <a name="langid-cell-character-section"></a>Célula LangID (Seção Character)

Indica o idioma no qual o texto foi inserido. 
  
## <a name="remarks"></a>Comentários

Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office oferecem suporte, consulte o tópico da célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties). 
  
Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.LangID [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCharacterLangID** <br/> |
   

