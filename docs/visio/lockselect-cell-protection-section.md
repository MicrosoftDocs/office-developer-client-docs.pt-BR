---
title: Célula LockSelect (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Impede uma forma de ser selecionada.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360666"
---
# <a name="lockselect-cell-protection-section"></a>Célula LockSelect (Seção Protection)

Impede uma forma de ser selecionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A forma não pode ser selecionada.  <br/> |
| FALSE  <br/> | A forma pode ser selecionada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para que a célula LockSelect tenha efeito, a caixa de seleção **Formas** deve estar marcada na caixa de diálogo **Proteger Documento**. 
  
Para fazer referência à célula LockSelect pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockSelect  <br/> |
   
Para fazer referência à célula LockSelect pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockSelect** <br/> |
   

