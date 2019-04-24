---
title: Célula Calendar (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Determina o calendário que é usado para dados da forma quando o tipo de dados é Data.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337503"
---
# <a name="calendar-cell-shape-data-section"></a>Célula Calendar (Seção Shape Data)

Determina o calendário que é usado para dados da forma quando o tipo de dados é Data.
  
## <a name="remarks"></a>Comentários

Os valores possíveis são: 0 (Ocidental), 1 (Islâmico árabe), 2 (Lunar hebraico), 3 (Calendário de Taiwan), 4 (Reinado do imperador japonês), 5 (Budista tailandês), 6 (Danki coreano), 7 (Era Saka), 8 (Transliteração inglesa) e 9 (Transliteração francesa). 
  
Para fazer referência à célula Calendar pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hélice.  *nome* . Calendário em que prop.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula Calendar pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice da linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsCalendar** <br/> |
   

