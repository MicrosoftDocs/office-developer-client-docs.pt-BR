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
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360589"
---
# <a name="doublestrikethrough-cell-character-section"></a>Célula DoubleStrikethrough (Seção Character)

Determina se o texto será formatado como tachado duplo.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula DoubleStrikethrough pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.DoubleStrikethrough[  *i*  ]            onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula DoubleStrikethrough pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice de linha:  <br/> |**visRowCharacter** +  *i*            onde  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

