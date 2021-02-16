---
title: Célula Font (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Representa o número da fonte utilizada para formatar o texto. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. O número 0 representa a fonte padrão, normalmente Arial.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438663"
---
# <a name="font-cell-character-section"></a>Célula Font (Seção Character)

Representa o número da fonte utilizada para formatar o texto. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. O número 0 representa a fonte padrão, normalmente Arial.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Font pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.Font[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula Font pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice de linha:  <br/> |**visRowCharacter** +  *i*            onde  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCharacterFont** <br/> |
   

