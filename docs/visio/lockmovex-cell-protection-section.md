---
title: Célula LockMoveX (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Protege a posição horizontal da forma para que ela não se mova horizontalmente.
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435856"
---
# <a name="lockmovex-cell-protection-section"></a>Célula LockMoveX (Seção Protection)

Protege a posição horizontal da forma para que ela não se mova horizontalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A posição horizontal está protegida.  <br/> |
| FALSE  <br/> | A posição horizontal não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockMoveX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockMoveX  <br/> |
   
Para fazer referência à célula LockMoveX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockMoveX** <br/> |
   

