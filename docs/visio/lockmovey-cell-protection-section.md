---
title: Célula LockMoveY (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Protege a posição vertical da forma para que ela não se mova verticalmente.
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348346"
---
# <a name="lockmovey-cell-protection-section"></a>Célula LockMoveY (Seção Protection)

Protege a posição vertical da forma para que ela não se mova verticalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A posição vertical está protegida.  <br/> |
| FALSE  <br/> | A posição vertical não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockMoveY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockMoveY  <br/> |
   
Para fazer referência à célula LockMoveY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockMoveY** <br/> |
   

