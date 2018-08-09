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
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772269"
---
# <a name="lockmovex-cell-protection-section"></a>Célula LockMoveX (Seção Protection)

Protege a posição horizontal da forma para que ela não se mova horizontalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A posição horizontal está protegida.  <br/> |
| FALSO  <br/> | A posição horizontal não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockMoveX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockMoveX  <br/> |
   
Para fazer referência à célula LockMoveX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockMoveX** <br/> |
   

