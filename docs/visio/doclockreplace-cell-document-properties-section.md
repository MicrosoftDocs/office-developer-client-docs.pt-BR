---
title: Célula DocLockReplace (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina se a interface do usuário da forma de substituição deve ser desabilitada para este documento.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413420"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Célula DocLockReplace (Seção Document Properties)

Determina se a interface do usuário da forma de substituição deve ser desabilitada para este documento. 
  
|||
|:-----|:-----|
|TRUE  <br/> |O **botão Substituir** Forma está es cinza na interface do usuário.  <br/> |
|FALSE  <br/> |O **botão Substituir** Forma está ativo na interface do usuário. Os usuários podem usar o recurso Substituir Forma neste documento.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **DocLockReplace** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DocLocReplace  <br/> |
   
Para fazer referência à célula **DocLocReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowDoc** <br/> |
| Índice de célula:  <br/> |**visDocLockReplace ** <br/> |
   

