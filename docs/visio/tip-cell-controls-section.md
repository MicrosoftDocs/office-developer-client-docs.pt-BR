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
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307718"
---
# <a name="tip-cell-controls-section"></a>Célula Tip (Seção Controls)

Representa uma sequência de texto descritiva exibida como uma dica de ferramenta quando o usuário posiciona o ponteiro do mouse sobre a alça de controle de uma forma. O aplicativo inclui automaticamente a dica entre aspas na célula, mas as aspas não são exibidas na dica de ferramenta.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Tip pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Menores.  *nome* . Controles Tipwhere.  *Name* é o nome da linha de controles.  <br/> |
   
Para fazer referência à célula Tip pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlTip** <br/> |
   

