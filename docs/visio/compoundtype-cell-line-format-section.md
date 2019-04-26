---
title: Célula CompoundType (Seção Formato da linha)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina o tipo composto da linha de uma forma.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359364"
---
# <a name="compoundtype-cell-line-format-section"></a>Célula CompoundType (Seção Formato da linha)

Determina o tipo composto da linha de uma forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Simples  <br/> |
|1  <br/> |Duplo  <br/> |
|2  <br/> |Espesso fino  <br/> |
|3  <br/> |Fino espesso  <br/> |
|4  <br/> |Tripla  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula **CompoundType** pelo nome de outra fórmula, pelo valor do atributo **N** de um elemento de **Célula** ou por um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | CompoundType  <br/> |
   
Para obter uma referência à célula **CompoundType** pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLine** <br/> |
| Índice de célula:  <br/> |**visCompoundType** <br/> |
   

