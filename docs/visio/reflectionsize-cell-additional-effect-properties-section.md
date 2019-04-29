---
title: Célula reflexões (seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: Determina o tamanho da reflexão em relação à forma, como uma porcentagem de 0,0 a 100,0%. Uma forma com um valor de 0% na célula reFlexõesize não tem uma reflexão; um valor de 100% exibe uma imagem espelho completa da forma.
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409073"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a>Célula reflexões (seção Additional Effect Properties)

Determina o tamanho da reflexão em relação à forma, como uma porcentagem de 0,0 a 100,0%. Uma forma com um valor de 0% na célula **** reflexõesize não tem uma reflexão; um valor de 100% exibe uma imagem espelho completa da forma. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **reflexões** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReflectionSize  <br/> |
   
Para fazer referência à célula **reflexões** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visReflectionSize** <br/> |
   

