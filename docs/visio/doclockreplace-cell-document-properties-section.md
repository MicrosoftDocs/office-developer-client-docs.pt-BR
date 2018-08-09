---
title: Célula DocLockReplace (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina se a forma de substituição da interface do usuário deve ser desabilitada para este documento.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771763"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Célula DocLockReplace (Seção Document Properties)

Determina se a forma de substituição da interface do usuário deve ser desabilitada para este documento. 
  
|||
|:-----|:-----|
|VERDADEIRO  <br/> |Botão **Substituir forma** estiver esmaecido na interface de usuário.  <br/> |
|FALSO  <br/> |Botão **Substituir forma** está ativo na interface de usuário. Os usuários podem usar o recurso de forma substituir neste documento.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **DocLockReplace** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DocLocReplace  <br/> |
   
Para obter uma referência à célula **DocLocReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |* * visDocLockReplace * * <br/> |
   

