---
title: Célula TheText (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Uma célula de evento avaliada quando a composição do texto ou o texto da forma é alterado.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326674"
---
# <a name="thetext-cell-events-section"></a>Célula TheText (Seção Events)

Uma célula de evento avaliada quando a composição do texto ou o texto da forma é alterado.
  
## <a name="remarks"></a>Comentários

As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula. É possível utilizar a célula TheText para disparar recálculos, por exemplo, recalcular a largura e a altura do texto com as funções TEXTWIDTH( ) e TEXTHEIGHT( ).
  
Para fazer referência à célula TheText pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TheText  <br/> |
   
Para fazer referência à célula TheText pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowEvent** <br/> |
| Índice da célula:  <br/> |**visEvtCellTheText** <br/> |
   

