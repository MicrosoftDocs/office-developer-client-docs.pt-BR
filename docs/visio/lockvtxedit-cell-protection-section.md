---
title: Célula LockVtxEdit (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Protege os vértices de uma forma impedindo-a de ser editada.
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358055"
---
# <a name="lockvtxedit-cell-protection-section"></a>Célula LockVtxEdit (Seção Protection)

Protege os vértices de uma forma impedindo-a de ser editada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |Os vértices não podem ser editados.  <br/> |
|FALSE  <br/> |Os vértices podem ser editados.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula LockVtxEdit pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockVtxEdit  <br/> |
   
Para obter uma referência para a célula LockVtxEdit pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLock** <br/> |
|Índice da célula:  <br/> |**visLockVtxEdit** <br/> |
   

