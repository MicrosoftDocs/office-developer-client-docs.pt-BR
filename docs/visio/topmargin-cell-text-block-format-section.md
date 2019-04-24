---
title: Célula TopMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1015
localization_priority: Normal
ms.assetid: c599b444-4d0e-a855-b04b-dd9dcaedf263
description: Determina a distância entre a borda superior do bloco de texto e a primeira linha do texto. O padrão é 4,0000 ponto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem superior será a mesma.
ms.openlocfilehash: 97d349fd4ddc3c76cda61e1ee7ce25909161e6fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280921"
---
# <a name="topmargin-cell-text-block-format-section"></a>Célula TopMargin (Seção Text Block Format)

Determina a distância entre a borda superior do bloco de texto e a primeira linha do texto. O padrão é 4,0000 ponto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem superior será a mesma.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TopMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TopMargin  <br/> |
   
Para fazer referência à célula TopMargin pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkTopMargin** <br/> |
   

