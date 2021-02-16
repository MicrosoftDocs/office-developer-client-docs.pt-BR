---
title: Célula PrintPageOrientation (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Determina se a página será impressa na orientação retrato ou paisagem.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434862"
---
# <a name="printpageorientation-cell-print-properties-section"></a>Célula PrintPageOrientation (Seção Print Properties)

Determina se a página será impressa na orientação retrato ou paisagem.
  
|**Valor**|**Orientation**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Mesmo que a impressora  <br/> |**visPPOSameAsPrinter** <br/> |
| 1   <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|2   <br/> |Paisagem  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>Comentários

Quando você insere novas páginas em um documento, essa configuração assume como padrão a configuração na página ativa.
  
Para fazer referência à célula PrintPageOrientation pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PrintPageOrientation  <br/> |
   
Para fazer referência à célula PrintPageOrientation pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

