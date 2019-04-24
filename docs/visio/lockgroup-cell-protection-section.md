---
title: Célula LockGroup (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Protege um grupo impedindo-o de ser desagrupado.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341789"
---
# <a name="lockgroup-cell-protection-section"></a>Célula LockGroup (Seção Protection)

Protege um grupo impedindo-o de ser desagrupado.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |O grupo não pode ser desagrupado.  <br/> |
|FALSE  <br/> |O grupo pode ser desagrupado.  <br/> |
   
## <a name="remarks"></a>Comentários

A definição do valor LockGroupCell como TRUE também impede a exclusão de formas que sejam membros do grupo.
  
Para obter uma referência para a célula LockGroup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockGroup  <br/> |
   
Para obter uma referência para a célula LockGroup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLock** <br/> |
|Índice da célula:  <br/> |**visLockGroup** <br/> |
   

