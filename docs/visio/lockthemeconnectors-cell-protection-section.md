---
title: Célula LockThemeConnectors (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impede que a célula ConnectorsSchemeIndex na linha Theme Properties seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438404"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Célula LockThemeConnectors (Seção Protection)

Impede que a **célula ConnectorsSchemeIndex** na linha **Theme Properties** seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A **célula ConnectorsSchemeIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente no ShapeSheet.  <br/> |
|FALSE  <br/> |A **célula ConnectorsSchemeIndex** pode ser alterada de seu valor atual por meio da interface do usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockThemeConnectors** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeConnectors  <br/> |
   
Para fazer referência à célula **LockThemeConnectors** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice de célula:  <br/> |**visLockThemeConnectors** <br/> |
   

