---
title: Célula RightMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Determina a distância entre a borda direita do bloco de texto e o texto contido nele. O padrão é 0,1 polegada.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326772"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Célula RightMargin (Seção Text Block Format)

Determina a distância entre a borda direita do bloco de texto e o texto contido nele. O padrão é 0,1 polegada.
  
## <a name="remarks"></a>Comentários

Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem direita será a mesma.
  
Para fazer referência à célula RightMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | RightMargin  <br/> |
   
Para fazer referência à célula RightMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkRightMargin** <br/> |
   

