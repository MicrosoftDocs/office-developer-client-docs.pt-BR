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
description: Controla o tipo de comportamento y-coordenadas da alça de controle irá exibir depois da alça ser movida. As fórmulas estão disponíveis.
ms.openlocfilehash: ee2a5e28748df603635f64c080119e28569f576a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773320"
---
# <a name="y-behavior-cell-controls-section"></a>Célula Y Behavior (Seção Controls)

Controla o tipo de comportamento *y* -coordenadas da alça de controle irá exibir depois da alça ser movida. As fórmulas estão disponíveis. 
  
|**Valor**|**Comportamento**|**Definição**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proporcional  <br/> | A alça de controle pode ser movida e ela se movimenta proporcionalmente à forma quando esta é alongada.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Protegida proporcionalmente  <br/> | A alça de controle se movimenta proporcionalmente à forma, mas a alça propriamente dita não pode ser movida.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Deslocar da borda inferior  <br/> | A alça de controle mantém uma distância de deslocamento constante da parte inferior da forma.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Deslocar do centro  <br/> | A alça de controle mantém uma distância de deslocamento constante do centro da forma.  <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> | Deslocar da borda superior  <br/> | A alça de controle mantém uma distância de deslocamento constante da parte superior da forma.  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | Proporcional, oculta  <br/> | Semelhante ao 0, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlProportionalHidden** <br/> |
| 6  <br/> | Protegida proporcionalmente, oculta  <br/> | Semelhante ao 1, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> | Deslocar da borda esquerda, oculta  <br/> | Semelhante ao 2, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8  <br/> | Deslocar do centro, oculta  <br/> | Semelhante ao 3, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> | Deslocar da borda direita, oculta  <br/> | Semelhante ao 4, mas a alça de controle não pode ser visualizada.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula Y Behavior pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome* . Controles de YConwhere.  *nome* é o nome da linha controles.  <br/> |
   
Para obter uma referência à célula X Behavior pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlYCon** <br/> |
   

