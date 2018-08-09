---
title: Célula BevelBottomType (Seção Bevel Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ac7b39d4-3942-4b23-b188-2c3f69e54929
description: Especifica o tipo de bisel baixo de bisel de uma forma.
ms.openlocfilehash: a0429011565d7a8f3ca0a7da76c08d309d5391f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771299"
---
# <a name="bevelbottomtype-cell-bevel-properties-section"></a>Célula BevelBottomType (Seção Bevel Properties)

Especifica o tipo de bisel baixo de bisel de uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Nenhum bisel  <br/> |
|1  <br/> |Bisel círculo  <br/> |
|2  <br/> |Bisel de baixo-relevo Relaxado  <br/> |
|3  <br/> |Bisel cruz  <br/> |
|4  <br/> |Bisel de inclinação interessante  <br/> |
|5  <br/> |Bisel ângulo  <br/> |
|6  <br/> |Arredondar suave bisel  <br/> |
|7  <br/> |Bisel convexo  <br/> |
|8  <br/> |Bisel inclinação  <br/> |
|9  <br/> |Bisel malha  <br/> |
|10  <br/> |Bisel talho  <br/> |
|11  <br/> |Disco rígido bisel de borda  <br/> |
|12  <br/> |Bisel art decô  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **BevelBottomType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** no formato de arquivo. vsdx, ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BevelBottomType  <br/> |
   
Para obter uma referência à célula **BevelBottomType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowBevelProperties** <br/> |
| Índice da célula:  <br/> |**visBevelBottomType** <br/> |
   

