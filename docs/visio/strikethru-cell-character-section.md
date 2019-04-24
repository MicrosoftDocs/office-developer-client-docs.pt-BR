---
title: Célula Strikethru (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Determina se o texto está formatado como tachado.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349333"
---
# <a name="strikethru-cell-character-section"></a>Célula Strikethru (Seção Character)

Determina se o texto está formatado como tachado.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |O texto está formatado como tachado.  <br/> |
|FALSE  <br/> |O texto não está formatado como tachado.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**). 
  
Para obter uma referência para a célula Strikethru pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char. Strikethru [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Strikethru pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterStrikethru** <br/> |
   

