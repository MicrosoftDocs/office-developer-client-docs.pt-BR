---
title: Célula Y Behavior (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
localization_priority: Normal
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: Controla o tipo de comportamento que a coordenada y da alça de controle exibirá depois que a alça for movida. Estas fórmulas estão disponíveis.
ms.openlocfilehash: bf8cbd490884244c92b68784dcbf041093539c94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413574"
---
# <a name="y-behavior-cell-controls-section"></a>Célula Y Behavior (Seção Controls)

Controla o tipo de comportamento que a coordenada  *y*  da alça de controle exibirá depois que a alça for movida. Estas fórmulas estão disponíveis. 
  
|**Valor**|**Comportamento**|**Definição**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proporcional  <br/> | A alça de controle pode ser movida e ela se movimenta proporcionalmente à forma quando esta é alongada.  <br/> |**visCtlProportional** <br/> |
| 1   <br/> | Protegida proporcionalmente  <br/> | A alça de controle se movimenta proporcionalmente à forma, mas a alça propriamente dita não pode ser movida.  <br/> |**visCtlLocked** <br/> |
| 2   <br/> | Deslocar da borda inferior  <br/> | A alça de controle mantém uma distância de deslocamento constante da parte inferior da forma.  <br/> |**visCtlOffsetMin** <br/> |
| 3   <br/> | Deslocar do centro  <br/> | A alça de controle mantém uma distância de deslocamento constante do centro da forma.  <br/> |**visCtlOffsetMid** <br/> |
| 4   <br/> | Deslocar da borda superior  <br/> | A alça de controle mantém uma distância de deslocamento constante da parte superior da forma.  <br/> |**visCtlOffsetMax** <br/> |
| 5   <br/> | Proporcional, oculta  <br/> | Semelhante ao 0, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlProportionalHidden** <br/> |
| 6   <br/> | Protegida proporcionalmente, oculta  <br/> | Semelhante ao 1, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | Deslocar da borda esquerda, oculta  <br/> | Semelhante ao 2, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | Deslocar do centro, oculta  <br/> | Semelhante ao 3, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | Deslocar da borda direita, oculta  <br/> | Semelhante ao 4, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Y Behavior pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome*  . Controles YConwhere.  *é*  o nome da linha de controles.  <br/> |
   
Para fazer referência à célula Y Behavior pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice de linha:  <br/> |**visRowControl**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlYCon** <br/> |
   

