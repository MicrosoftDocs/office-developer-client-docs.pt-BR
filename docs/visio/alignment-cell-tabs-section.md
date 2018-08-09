---
title: Célula Alignment (Seção Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Especifica o alinhamento de tabulação.
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771254"
---
# <a name="alignment-cell-tabs-section"></a>Célula Alignment (Seção Tabs)

Especifica o alinhamento de tabulação.
  
|**Valor**|**Alignment**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | À esquerda  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Centralizar  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Direita  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Decimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Vírgula  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Alignment pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Guias.  *ij* onde *i e j =* < 1 >, 2, 3  <br/> |
   
Para fazer referência à célula Alignment pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTab** <br/> |
| Índice da linha:  <br/> |**visRowTab +** *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

