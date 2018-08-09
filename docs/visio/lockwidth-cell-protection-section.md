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
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772277"
---
# <a name="lockwidth-cell-protection-section"></a>Célula LockWidth (Seção Protection)

Protege a largura da forma para que ela não seja alterada quando a forma for dimensionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A largura está protegida.  <br/> |
| FALSO  <br/> | A largura não está protegida.  <br/> |
   
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
   

