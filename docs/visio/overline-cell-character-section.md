---
title: Célula Overline (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Determina se o texto conterá uma linha acima dele.
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772438"
---
# <a name="overline-cell-character-section"></a>Célula Overline (Seção Character)

Determina se o texto conterá uma linha acima dele.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O texto contém uma linha acima dele.  <br/> |
|FALSO  <br/> |O texto não contém uma linha acima dele.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**). 
  
Para obter uma referência para a célula Overline pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.Overline [ *i* ] onde *i* = < 1 >, 2. 3...  <br/> |
   
Para obter uma referência para a célula Overline pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterOverline** <br/> |
   

