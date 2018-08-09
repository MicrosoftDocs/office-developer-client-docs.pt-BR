---
title: Célula LockThemeConnectors (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impede que a célula ConnectorsSchemeIndex na linha de propriedades do tema que está sendo alterado a aplicação de um novo tema ou selecionando um novo esquema de conector. Não impede que usuários editando manualmente esse valor na ShapeSheet.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772270"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Célula LockThemeConnectors (Seção Protection)

Impede que a célula **ConnectorsSchemeIndex** na linha de **Propriedades do tema** que está sendo alterado a aplicação de um novo tema ou selecionando um novo esquema de conector. Não impede que usuários editando manualmente esse valor na ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A célula **ConnectorsSchemeIndex** não pode ser alterada de seu valor atual, a menos que alterado na ShapeSheet diretamente.  <br/> |
|FALSO  <br/> |A célula **ConnectorsSchemeIndex** pode ser alterada de seu valor atual por meio da interface do usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockThemeConnectors** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeConnectors  <br/> |
   
Para obter uma referência à célula **LockThemeConnectors** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockThemeConnectors** <br/> |
   

