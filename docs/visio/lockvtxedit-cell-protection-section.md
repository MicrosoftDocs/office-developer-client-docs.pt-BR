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
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772285"
---
# <a name="lockvtxedit-cell-protection-section"></a>Célula LockVtxEdit (Seção Protection)

Protege os vértices de uma forma impedindo-a de ser editada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Os vértices não podem ser editados.  <br/> |
|FALSO  <br/> |Os vértices podem ser editados.  <br/> |
   
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
   

