---
title: Célula LeftMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Determina a distância entre a borda esquerda do bloco de texto e o texto contido nele. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem esquerda será a mesma.
ms.openlocfilehash: d24ba33bffea1529490b49e105fec5d01cd828b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772177"
---
# <a name="leftmargin-cell-text-block-format-section"></a>Célula LeftMargin (Seção Text Block Format)

Determina a distância entre a borda esquerda do bloco de texto e o texto contido nele. O padrão é 0,1 polegada. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem esquerda será a mesma.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula LeftMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LeftMargin  <br/> |
   
Para fazer referência à célula LeftMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkLeftMargin** <br/> |
   

