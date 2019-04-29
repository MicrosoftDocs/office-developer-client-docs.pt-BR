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
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414015"
---
# <a name="pos-cell-character-section"></a>Célula Pos (Seção Character)

Determina a posição do texto da forma em relação à linha de base.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Posição normal  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Sobrescrito  <br/> |**visPosSuper** <br/> |
| duas  <br/> | Subscrito  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Pos pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char. pos [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Pos pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice de linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCharacterPos** <br/> |
   

