---
title: Célula LockVariation (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um Boolean.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358062"
---
# <a name="lockvariation-cell-protection-section"></a>Célula LockVariation (seção Protection)

Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |A variação atual aplicada à página ou forma não pode ser alterada.  <br/> |
|FALSE  <br/> |A variação da página ou da forma pode ser alterada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **LockVariation** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockVariation  <br/> |
   
Para obter uma referência para a célula **LockVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockVariation** <br/> |
   

