---
title: Célula LockReplace (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica se uma forma pode participar de uma operação de substituição (como uma forma de destino ou de substituição).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348220"
---
# <a name="lockreplace-cell-protection-section"></a>Célula LockReplace (seção Protection)

Indica se uma forma pode participar de uma operação de substituição (como uma forma de destino ou de substituição). 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |A forma não pode ser substituída ou usada como uma forma de substituição.  <br/> Para uma forma na tela, o botão **alterar forma** é desabilitado quando a forma é selecionada.  <br/> Para uma forma em um estêncil, a forma não aparecerá como uma forma de substituição quando o botão **alterar forma** for clicado.  <br/> |
|FALSE  <br/> |A forma pode ser substituída ou usada como uma forma de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **LockReplace** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockReplace  <br/> |
   
Para obter uma referência para a célula **LockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockReplace** <br/> |
   

