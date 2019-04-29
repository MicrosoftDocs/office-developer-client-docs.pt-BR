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
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423136"
---
# <a name="lockdelete-cell-protection-section"></a>Célula LockDelete (Seção Protection)

Protege a forma impedindo-a de ser excluída.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma não pode ser excluída.  <br/> |
| FALSE  <br/> | A forma pode ser excluída.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockDelete pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockDelete  <br/> |
   
Para fazer referência à célula LockDelete pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockDelete** <br/> |
   

