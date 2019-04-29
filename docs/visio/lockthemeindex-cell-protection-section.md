---
title: Célula LockThemeIndex (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impede que ThemeIndex célula da linha de propriedades do tema seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411236"
---
# <a name="lockthemeindex-cell-protection-section"></a>Célula LockThemeIndex (seção Protection)

Impede que **ThemeIndex** célula da linha de **Propriedades do tema** seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A célula **ThemeIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente na ShapeSheet.  <br/> |
|FALSE  <br/> |A célula **ThemeIndex** pode ser alterada de seu valor atual quando o tema é alterado.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **LockThemeIndex** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeIndex  <br/> |
   
Para obter uma referência para a célula **LockThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockThemeIndex** <br/> |
   

