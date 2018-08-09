---
title: Célula Can Glue (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Determina se é possível associar uma alça de controle a outras formas.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771422"
---
# <a name="can-glue-cell-controls-section"></a>Célula Can Glue (Seção Controls)

Determina se é possível associar uma alça de controle a outras formas.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | É possível associar a alça de controle.  <br/> |
| FALSO  <br/> | Não é possível associar a alça de controle.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Can Glue pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome* . Controles de CanGluewhere.  *nome* é o nome da linha controles.  <br/> |
   
Para fazer referência à célula Can Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2,...  <br/> |
| Índice da célula:  <br/> |**visCtlGlue** <br/> |
   

