---
title: Célula Spacing (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Controla a quantidade de espaço entre dois ou mais caracteres. O espaço pode ser adicionado ou subtraído em incrementos de ponto de 1/20.
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334899"
---
# <a name="spacing-cell-character-section"></a>Célula Spacing (Seção Character)

Controla a quantidade de espaço entre dois ou mais caracteres. O espaço pode ser adicionado ou subtraído em incrementos de ponto de 1/20.
  
## <a name="remarks"></a>Comentários

Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**). 
  
Para obter uma referência para a célula Spacing pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char. Letterspace [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Spacing pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterLetterspace** <br/> |
   

