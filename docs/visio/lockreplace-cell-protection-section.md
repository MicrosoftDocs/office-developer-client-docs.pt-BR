---
title: Célula LockReplace (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica se uma forma pode participar de uma operação de substituição (como um destino ou uma forma de substituição).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404138"
---
# <a name="lockreplace-cell-protection-section"></a>Célula LockReplace (Seção Protection)

Indica se uma forma pode participar de uma operação de substituição (como um destino ou uma forma de substituição). 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A forma não pode ser substituída ou usada como uma forma de substituição.  <br/> Para uma forma na tela, o **botão Alterar** Forma é desabilitado quando a forma é selecionada.  <br/> Para uma forma em um estêncil, a forma não aparece como uma forma substituta quando o botão Alterar **Forma** é clicado.  <br/> |
|FALSE  <br/> |A forma pode ser substituída ou usada como uma forma de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockReplace** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockReplace  <br/> |
   
Para fazer referência à **célula LockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice de célula:  <br/> |**visLockReplace** <br/> |
   

