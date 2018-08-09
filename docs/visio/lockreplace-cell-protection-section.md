---
title: Célula LockReplace (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica se uma forma pode participar de uma operação de substituição (como um destino ou uma forma de substituição).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772253"
---
# <a name="lockreplace-cell-protection-section"></a>Célula LockReplace (Seção Protection)

Indica se uma forma pode participar de uma operação de substituição (como um destino ou uma forma de substituição). 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A forma não pode ser substituída ou a ser usada como uma forma de substituição.  <br/> Para uma forma na tela de desenho, o botão **Alterar forma** é desabilitado quando a forma é selecionada.  <br/> Para uma forma em um estêncil, a forma não é exibido como uma forma de substituição quando o botão **Alterar forma** for clicado.  <br/> |
|FALSO  <br/> |A forma pode ser substituída ou usada como uma forma de substituição.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LockReplace** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockReplace  <br/> |
   
Para obter uma referência à célula **LockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockReplace** <br/> |
   

