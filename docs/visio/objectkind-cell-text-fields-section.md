---
title: Célula ObjectKind (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indica o tipo de campo de texto.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772421"
---
# <a name="objectkind-cell-text-fields-section"></a>Célula ObjectKind (Seção Text Fields)

Indica o tipo de campo de texto.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |Horizontal em vertical  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Comentários

Os tipos de campo de texto podem ser um destes:
  
- Padrão: indica que o campo foi inserido pela categoria de campo.
    
- Horizontal em vertical: indica que o campo é de texto horizontal definido em texto vertical.
    
Para fazer referência à célula ObjectKind pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Fields.ObjectKind [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula ObjectKind pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTextField** <br/> |
| Índice da linha:  <br/> |**visRowField** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visFieldObjectKind** <br/> |
   

