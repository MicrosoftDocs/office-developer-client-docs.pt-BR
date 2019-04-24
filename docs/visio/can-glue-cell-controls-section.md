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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337251"
---
# <a name="can-glue-cell-controls-section"></a>Célula Can Glue (Seção Controls)

Determina se é possível associar uma alça de controle a outras formas.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | É possível associar a alça de controle.  <br/> |
| FALSE  <br/> | Não é possível associar a alça de controle.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Can Glue pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Menores.  *nome* . Controles CanGluewhere.  *Name* é o nome da linha de controles.  <br/> |
   
Para fazer referência à célula Can Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2,...  <br/> |
| Índice da célula:  <br/> |**visCtlGlue** <br/> |
   

