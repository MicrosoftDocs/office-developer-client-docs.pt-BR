---
title: Célula ReplaceLockShapeData (seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. O ReplaceLockShapeData determina se os dados da forma da forma mestre substituirão todos os dados da forma da forma que está sendo substituída.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348339"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Célula ReplaceLockShapeData (seção Change Shape Behavior)

Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. O **ReplaceLockShapeData** determina se os dados da forma da forma mestre substituirão todos os dados da forma da forma que está sendo substituída. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|1 (TRUE)  <br/> |Todas as linhas e valores da seção de **dados da forma** da forma mestre são copiados para a forma de substituição e quaisquer valores locais da forma antiga que está sendo substituído são descartados.  <br/> |
|0 (FALSO)  <br/> |As linhas e os valores da seção de **dados da forma** da forma mestre são copiados para a forma de substituição. Qualquer linha na seção **Shape data** da forma antiga com valores locais é transferida para a forma de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **ReplaceLockShapeData** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockShapeData  <br/> |
   
Para obter uma referência para a célula **ReplaceLockShapeData** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceLockShapeData** <br/> |
   

