---
title: Célula Tip (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Representa uma sequência de texto descritiva exibida como uma dica de ferramenta quando o usuário posiciona o ponteiro do mouse sobre a alça de controle de uma forma. O aplicativo inclui automaticamente a dica entre aspas na célula, mas as aspas não são exibidas na dica de ferramenta.
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773156"
---
# <a name="tip-cell-controls-section"></a>Célula Tip (Seção Controls)

Representa uma sequência de texto descritiva exibida como uma dica de ferramenta quando o usuário posiciona o ponteiro do mouse sobre a alça de controle de uma forma. O aplicativo inclui automaticamente a dica entre aspas na célula, mas as aspas não são exibidas na dica de ferramenta.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Tip pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome* . Controles de Tipwhere.  *nome* é o nome da linha controles.  <br/> |
   
Para fazer referência à célula Tip pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlTip** <br/> |
   

