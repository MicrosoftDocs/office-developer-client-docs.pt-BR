---
title: Célula Calendar (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Determina o calendário a ser usado quando a fórmula de uma célula contém informações de Data.
ms.openlocfilehash: 2bca91fd2efc283bcc8f2c5037c4d81dd9bcffc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771427"
---
# <a name="calendar-cell-miscellaneous-section"></a>Célula Calendar (Seção Miscellaneous)

Determina o calendário a ser usado quando a fórmula de uma célula contém informações de Data.
  
## <a name="remarks"></a>Comentários

Os valores possíveis são: 0 (Ocidental), 1 (Islâmico árabe), 2 (Lunar hebraico), 3 (Calendário de Taiwan), 4 (Reinado do imperador japonês), 5 (Budista tailandês), 6 (Danki coreano), 7 (Era Saka), 8 (Transliteração inglesa) e 9 (Transliteração francesa). 
  
Para obter uma referência à célula Calendar pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Calendar  <br/> |
   
Para obter uma referência à célula Calendar pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visObjCalendar** <br/> |
   

