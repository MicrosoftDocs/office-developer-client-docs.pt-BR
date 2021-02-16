---
title: Célula LockThemeFonts (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impede que a célula FontIndex na linha Theme Properties seja alterada aplicando um novo tema. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421225"
---
# <a name="lockthemefonts-cell-protection-section"></a>Célula LockThemeFonts (Seção Protection)

Impede que **a célula FontIndex** na linha **Theme Properties** seja alterada aplicando um novo tema. Não impede que os usuários editem manualmente esse valor no ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A **célula FontIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente no ShapeSheet.  <br/> |
|FALSE  <br/> |A **célula FontIndex** pode ser alterada de seu valor atual quando o tema é alterado.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockThemeFonts** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeFonts  <br/> |
   
Para fazer referência à **célula LockThemeFonts** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice de célula:  <br/> |**visLockThemeFonts** <br/> |
   

