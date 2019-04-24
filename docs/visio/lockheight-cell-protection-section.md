---
title: Célula LockHeight (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Protege a altura da forma para que ela não seja alterada quando a forma for dimensionada.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341773"
---
# <a name="lockheight-cell-protection-section"></a>Célula LockHeight (Seção Protection)

Protege a altura da forma para que ela não seja alterada quando a forma for dimensionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A altura está protegida.  <br/> |
| FALSE  <br/> | A altura não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockHeight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockHeight  <br/> |
   
Para fazer referência à célula LockHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockHeight** <br/> |
   

