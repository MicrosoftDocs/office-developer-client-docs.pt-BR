---
title: Célula DoubleStrikethrough (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Determina se o texto será formatado como tachado duplo.
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771770"
---
# <a name="doublestrikethrough-cell-character-section"></a>Célula DoubleStrikethrough (Seção Character)

Determina se o texto será formatado como tachado duplo.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula DoubleStrikethrough pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.DoubleStrikethrough [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula DoubleStrikethrough pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

