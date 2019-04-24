---
title: Célula LockThemeConnectors (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impede que a célula ConnectorsSchemeIndex na linha de propriedades do tema seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348234"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Célula LockThemeConnectors (seção Protection)

Impede que a célula **ConnectorsSchemeIndex** na linha de **Propriedades do tema** seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |A célula **ConnectorsSchemeIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente na ShapeSheet.  <br/> |
|FALSE  <br/> |A célula **ConnectorsSchemeIndex** pode ser alterada de seu valor atual por meio da interface do usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **LockThemeConnectors** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockThemeConnectors  <br/> |
   
Para obter uma referência para a célula **LockThemeConnectors** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockThemeConnectors** <br/> |
   

