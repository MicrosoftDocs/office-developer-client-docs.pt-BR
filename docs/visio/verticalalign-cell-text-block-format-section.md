---
title: Célula VerticalAlign (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Determina o alinhamento vertical do texto no bloco de texto.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425789"
---
# <a name="verticalalign-cell-text-block-format-section"></a>Célula VerticalAlign (Seção Text Block Format)

Determina o alinhamento vertical do texto no bloco de texto.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Início  <br/> |**visVertTop** <br/> |
| 1  <br/> | Middleware  <br/> |**visVertMiddle** <br/> |
| duas  <br/> | Inferior  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula VerticalAlign pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | VerticalAlign  <br/> |
   
Para fazer referência à célula VerticalAlign pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

