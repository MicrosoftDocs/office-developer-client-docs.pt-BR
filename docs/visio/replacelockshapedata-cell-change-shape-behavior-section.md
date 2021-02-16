---
title: Célula ReplaceLockShapeData (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica se os valores das células especificadas em uma forma mestra substituem os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. ReplaceLockShapeData determina se os dados da forma mestra sobrescrevem todos os dados da forma que está sendo substituída.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408870"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Célula ReplaceLockShapeData (Seção Change Shape Behavior)

Indica se os valores das células especificadas em uma forma mestra substituem os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. **ReplaceLockShapeData** determina se os dados da forma mestra sobrescrevem todos os dados da forma que está sendo substituída. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|1 (VERDADEIRO)  <br/> |Todas as linhas e valores da seção **Shape Data** da forma mestra são copiados para a forma substituta e quaisquer valores locais da forma antiga que está sendo substituída são descartados.  <br/> |
|0 (FALSO)  <br/> |As linhas e os valores da **seção Shape Data** da forma mestra são copiados para a forma de substituição. Todas as linhas na **seção Shape Data** da forma antiga com valores locais são transferidas para a forma de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ReplaceLockShapeData** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockShapeData  <br/> |
   
Para fazer referência à célula **ReplaceLockShapeData** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de célula:  <br/> |**visReplaceLockShapeData** <br/> |
   

