---
title: Célula LockWidth (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Protege a largura da forma para que ela não seja alterada quando a forma for dimensionada.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314830"
---
# <a name="lockwidth-cell-protection-section"></a>Célula LockWidth (Seção Protection)

Protege a largura da forma para que ela não seja alterada quando a forma for dimensionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A largura está protegida.  <br/> |
| FALSE  <br/> | A largura não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockWidth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockWidth  <br/> |
   
Para fazer referência à célula LockWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockWidth** <br/> |
   

