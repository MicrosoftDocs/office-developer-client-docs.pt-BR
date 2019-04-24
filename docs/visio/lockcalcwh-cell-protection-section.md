---
title: Célula LockCalcWH (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Bloqueia um retângulo de seleção de uma forma para que ele não seja recalculado quando uma vértice for editada ou um tipo de linha for alterado na seção Geometry.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359630"
---
# <a name="lockcalcwh-cell-protection-section"></a>Célula LockCalcWH (Seção Protection)

Bloqueia um retângulo de seleção de uma forma para que ele não seja recalculado quando uma vértice for editada ou um tipo de linha for alterado na seção Geometry.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A largura e a altura não podem ser recalculadas.  <br/> |
| FALSE  <br/> | A largura e a altura podem ser recalculadas.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockCalcWH pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockCalcWH  <br/> |
   
Para fazer referência à célula LockCalcWH pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockCalcWH** <br/> |
   

