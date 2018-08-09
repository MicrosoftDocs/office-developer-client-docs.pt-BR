---
title: Célula BottomMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: Determina a distância entre a borda inferior do bloco de texto e a última linha do texto. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem inferior será a mesma.
ms.openlocfilehash: f3515485b0418ffeaf55910a972e1e480f428e4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771416"
---
# <a name="bottommargin-cell-text-block-format-section"></a>Célula BottomMargin (Seção Text Block Format)

Determina a distância entre a borda inferior do bloco de texto e a última linha do texto. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem inferior será a mesma.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula BottomMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BottomMargin  <br/> |
   
Para fazer referência à célula BottomMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkBottomMargin** <br/> |
   

