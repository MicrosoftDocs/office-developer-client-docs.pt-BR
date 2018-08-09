---
title: Célula LockThemeFonts (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impede que a célula FontIndex na linha de propriedades do tema que está sendo alterada aplicando um novo tema. Não impede que usuários editando manualmente esse valor na ShapeSheet.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772291"
---
# <a name="lockthemefonts-cell-protection-section"></a>Célula LockThemeFonts (Seção Protection)

Impede que a célula **FontIndex** na linha de **Propriedades do tema** que está sendo alterada aplicando um novo tema. Não impede que usuários editando manualmente esse valor na ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A célula **FontIndex** não pode ser alterada de seu valor atual, a menos que alterado na ShapeSheet diretamente.  <br/> |
|FALSO  <br/> |A célula **FontIndex** pode ser alterada de seu valor atual, quando o tema é alterado.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockThemeFonts** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeFonts  <br/> |
   
Para obter uma referência à célula **LockThemeFonts** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockThemeFonts** <br/> |
   

