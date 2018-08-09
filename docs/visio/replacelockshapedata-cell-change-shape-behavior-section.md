---
title: Célula ReplaceLockShapeData (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. O ReplaceLockShapeData determina se os dados da forma da forma mestra substitui todos os dados da forma da forma que está sendo substituído.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772716"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Célula ReplaceLockShapeData (Seção Change Shape Behavior)

Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. O **ReplaceLockShapeData** determina se os dados da forma da forma mestra substitui todos os dados da forma da forma que está sendo substituído. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|1 (VERDADEIRO)  <br/> |Todas as linhas e os valores da seção **Shape Data** da forma mestra são copiados para a forma de substituição e quaisquer valores locais da forma que está sendo substituído antiga serão descartados.  <br/> |
|0 (FALSO)  <br/> |As linhas e os valores da seção **Shape Data** da forma mestra são copiados para a forma de substituição. Qualquer linha na seção **Dados da forma** da forma antiga com valores locais é transferida para a forma de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ReplaceLockShapeData** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockShapeData  <br/> |
   
Para obter uma referência à célula **ReplaceLockShapeData** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceLockShapeData** <br/> |
   

