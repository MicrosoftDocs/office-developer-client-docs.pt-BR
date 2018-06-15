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
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772272"
---
# <a name="lockselect-cell-protection-section"></a>Célula LockSelect (Seção Protection)

Impede uma forma de ser selecionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma não pode ser selecionada.  <br/> |
| FALSO  <br/> | A forma pode ser selecionada.  <br/> |
   
## <a name="remarks"></a>Comentários

Em ordem para a célula LockSelect tenha efeito, a caixa de seleção **formas** deve ser selecionada na caixa de diálogo **Proteger documento** . 
  
Para obter uma referência à célula LockSelect pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockSelect  <br/> |
   
Para obter uma referência à célula LockSelect pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockSelect** <br/> |
   

