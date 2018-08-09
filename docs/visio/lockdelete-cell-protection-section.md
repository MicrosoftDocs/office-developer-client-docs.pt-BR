---
title: Célula LockDelete (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Protege a forma impedindo-a de ser excluída.
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772243"
---
# <a name="lockdelete-cell-protection-section"></a>Célula LockDelete (Seção Protection)

Protege a forma impedindo-a de ser excluída.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma não pode ser excluída.  <br/> |
| FALSO  <br/> | A forma pode ser excluída.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockDelete pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockDelete  <br/> |
   
Para fazer referência à célula LockDelete pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockDelete** <br/> |
   

