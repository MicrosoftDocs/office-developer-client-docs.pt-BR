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
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425537"
---
# <a name="alignment-cell-tabs-section"></a>Célula Alignment (Seção Tabs)

Especifica o alinhamento de tabulação.
  
|**Valor**|**Alignment**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Esquerda  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Centro  <br/> |**visTabStopCenter** <br/> |
| duas  <br/> | À direita  <br/> |**visTabStopRight** <br/> |
| 3D  <br/> | Decimal  <br/> |**visTabStopDecimal** <br/> |
| 4   <br/> | Ponto  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Alignment pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Tabula.  *IJ* onde *i e j =* <1>, 2, 3  <br/> |
   
Para fazer referência à célula Alignment pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTab** <br/> |
| Índice de linha:  <br/> |**visRowTab +** *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

