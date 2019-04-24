---
title: Célula TextDirection (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Determina a direção dos caracteres em um bloco de texto.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332354"
---
# <a name="textdirection-cell-text-block-format-section"></a>Célula TextDirection (Seção Text Block Format)

Determina a direção dos caracteres em um bloco de texto.
  
|**Valor**|**Direction**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Horizontal  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Vertical  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Comentários

Na versão 5.0 do Visio, na linha de produtos japoneses, o valor dessa célula era armazenada na célula VerticalText, na seção Miscellaneous.
  
Para fazer referência à célula TextDirection pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TextDirection  <br/> |
   
Para fazer referência à célula TextDirection pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkDirection** <br/> |
   

