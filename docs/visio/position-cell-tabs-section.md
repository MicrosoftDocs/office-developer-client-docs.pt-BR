---
title: Célula Position (Seção Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Especifica a posição de uma parada de tabulação. A posição da tabulação não depende da escala do desenho. Se o desenho estiver em escala, a posição da tabulação será a mesma.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409927"
---
# <a name="position-cell-tabs-section"></a>Célula Position (Seção Tabs)

Especifica a posição de uma parada de tabulação. A posição da tabulação não depende da escala do desenho. Se o desenho estiver em escala, a posição da tabulação será a mesma.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Position pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Guias.  *ij*            onde  *i*  e  *j*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Position pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTab** <br/> |
| Índice de linha:  <br/> |**visRowTab**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> | (*j*  *3) + **visTabPos** <br/> |
   

