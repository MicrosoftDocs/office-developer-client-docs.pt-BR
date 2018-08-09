---
title: Célula Pos (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Determina a posição do texto da forma em relação à linha de base.
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772583"
---
# <a name="pos-cell-character-section"></a>Célula Pos (Seção Character)

Determina a posição do texto da forma em relação à linha de base.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Posição normal  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Sobrescrito  <br/> |**visPosSuper** <br/> |
| 2  <br/> | Subscrito  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Pos pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.Pos [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Pos pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCharacterPos** <br/> |
   

