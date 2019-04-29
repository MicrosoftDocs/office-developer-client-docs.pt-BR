---
title: Célula ReplaceLockFormat (seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. Se a célula ReplaceLockFormat de uma forma mestre for definida como TRUE (1), os valores de formatação do mestre substituirão todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427231"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Célula ReplaceLockFormat (seção Change Shape Behavior)

Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. Se a célula **ReplaceLockFormat** de uma forma mestre for definida como true (1), os valores de formatação do mestre substituirão todos os valores correspondentes de uma forma que está sendo substituído pelo mestre. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Se a célula **ReplaceLockFormat** de uma forma mestre for definida como true, os valores de formatação do mestre substituirão todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.  <br/> |
|FALSE  <br/> |Se a célula **ReplaceLockFormat** de uma forma mestre estiver definida como false, a forma de substituição conterá os valores de formatação local da forma antiga após a operação de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

A célula **ReplaceLockFormat** determina se a forma mestre substituirá os valores de formatação local das células nas seções a seguir durante uma operação de substituição de forma: 
  
- Seção **Fill Format** 
    
- Seção **line Format** 
    
- Seção **Style rápido** 
    
- Seção **Theme Properties** 
    
- Seção **Propriedades** de gradiente 
    
- Seção de **Propriedades de bisel** 
    
- Seção **Additional Effect Properties** 
    
- Seção paradas de gradiente de **linha** 
    
- Seção **Fill gradientout** 
    
Para obter uma referência para a célula **ReplaceLockFormat** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockFormat  <br/> |
   
Para obter uma referência para a célula **ReplaceLockFormat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceLockFormat** <br/> |
   

