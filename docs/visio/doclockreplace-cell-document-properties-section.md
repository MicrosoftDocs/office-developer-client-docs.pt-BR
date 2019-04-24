---
title: Célula DocLockReplace (seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina se a interface do usuário substituir forma deve ser desabilitada para este documento.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338602"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Célula DocLockReplace (seção Document Properties)

Determina se a interface do usuário substituir forma deve ser desabilitada para este documento. 
  
|||
|:-----|:-----|
|TRUE  <br/> |O botão **substituir forma** está ESMAECIDO na interface do usuário.  <br/> |
|FALSE  <br/> |O botão **substituir forma** está ativo na interface do usuário. Os usuários podem usar o recurso substituir forma neste documento.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **DocLockReplace** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DocLocReplace  <br/> |
   
Para obter uma referência para a célula **DocLocReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |* * visDocLockReplace * * <br/> |
   

