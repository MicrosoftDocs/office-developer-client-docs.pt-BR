---
title: Célula Format (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Especifica a formatação de um campo de texto que pode ser uma sequência de caracteres, um número, uma data ou uma hora, uma duração ou uma moeda.
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771933"
---
# <a name="format-cell-text-fields-section"></a>Célula Format (Seção Text Fields)

Especifica a formatação de um campo de texto que pode ser uma sequência de caracteres, um número, uma data ou uma hora, uma duração ou uma moeda.
  
## <a name="remarks"></a>Comentários

Se o valor da célula Type for 0, 2, 5, 6 ou 7 (cadeia de caracteres, número, data ou hora, duração ou moeda, respectivamente), especifique uma figura de formatação apropriada para o tipo de dados. Por exemplo, a figura de formatação "# #/4 UU" formata o número 12,43 pol. como 12 2/4 POLEGADAS. Para obter mais informações sobre como especificar uma figura de formatação, consulte [Sobre figuras de formatação](about-format-pictures.md).
  
Um número (Tipo = 2) pode representar uma dimensão, uma grandeza escalar, um ângulo, uma data, uma hora ou uma moeda. Para garantir que um número de entrada seja sempre avaliado como uma data, hora ou moeda, utilize as funções DATETIME ou CY na célula Format em vez de uma figura de formatação.
  
Para fazer referência à célula Format pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Fields.Format [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Format pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTextField** <br/> |
| Índice da linha:  <br/> |**visRowField** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visFieldFormat** <br/> |
   

