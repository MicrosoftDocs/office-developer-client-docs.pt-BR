---
title: Célula DontMoveChildren (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Determina se é possível arrastar formas em um grupo usando o mouse.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338581"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>Célula DontMoveChildren (Seção Group Properties)

Determina se é possível arrastar formas em um grupo usando o mouse.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | Não permite que as formas em um grupo sejam arrastadas usando o mouse.  <br/> |
| FALSE  <br/> | Permite que as formas em um grupo sejam arrastadas usando o mouse.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o valor desta célula é VERDADEIRO, é possível também inverter, girar, redimensionar ou reposicionar as formas em grupos usando outros métodos.
  
O valor da célula é VERDADEIRO para grupos em mestres e em instâncias de mestres criados nas versões do Visio anteriores à versão de 2000.
  
Para fazer referência à célula DontMoveChildren pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DontMoveChildren  <br/> |
   
Para fazer referência à célula DontMoveChildren pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGroup** <br/> |
| Índice da célula:  <br/> |**visGroupDontMoveChildren** <br/> |
   

