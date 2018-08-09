---
title: Célula LockThemeIndex (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impede que a célula ThemeIndex na linha de propriedades do tema sejam alterados aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que usuários editando manualmente esse valor na ShapeSheet.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772273"
---
# <a name="lockthemeindex-cell-protection-section"></a>Célula LockThemeIndex (Seção Protection)

Impede que a célula **ThemeIndex** na linha de **Propriedades do tema** sejam alterados aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que usuários editando manualmente esse valor na ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A célula **ThemeIndex** não pode ser alterada de seu valor atual, a menos que alterado na ShapeSheet diretamente.  <br/> |
|FALSO  <br/> |A célula **ThemeIndex** pode ser alterada de seu valor atual, quando o tema é alterado.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockThemeIndex** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeIndex  <br/> |
   
Para obter uma referência à célula **LockThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockThemeIndex** <br/> |
   

