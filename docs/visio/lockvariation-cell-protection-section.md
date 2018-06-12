---
title: Célula LockVariation (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um valor booleano.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772287"
---
# <a name="lockvariation-cell-protection-section"></a>Célula LockVariation (seção Protection)

Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um valor booleano.
  
|||
|:-----|:-----|
|VERDADEIRO  <br/> |A variação atual aplicada à forma ou página não pode ser alterada.  <br/> |
|FALSO  <br/> |A variação da página ou forma pode ser alterada.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Para fazer referência à célula **LockVariation** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockVariation  <br/> |
   
Para obter uma referência à célula **LockVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockVariation** <br/> |
   

