---
title: Célula Style (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Mostra a formatação de caracteres aplicada a um intervalo de texto no bloco de texto da forma.
ms.openlocfilehash: 349bdc42485aa511011aeb85a43f1ab3e4ea853d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411425"
---
# <a name="style-cell-character-section"></a>Célula Style (Seção Character)

Mostra a formatação de caracteres aplicada a um intervalo de texto no bloco de texto da forma.
  
|**Estilo**|**Valor**|**Constante de automação**|
|:-----|:-----|:-----|
| Negrito  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Itálico  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Sublinhado  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Caixa alta  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>Comentários

A célula Style conterá informações de formatação aplicada a um subintervalo de texto de uma forma se a seção Characters contiver diversas linhas. Caso contrário, ela conterá informações de formatação para todo o texto da forma.
  
O valor representa um número binário no qual cada bit indica um estilo de caractere. Por exemplo, um valor de 3 representa o texto formatado em itálico e negrito. Se o valor da célula Style for 0, o texto não terá formatação. Você pode testar um formato específico usando funções BIT \* booleanas. Consulte a documentação de programação para obter detalhes sobre essas funções.
  
Para fazer referência à célula Style pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.Style[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula Style pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice de linha:  <br/> |**visRowCharacter** +  *i*            onde  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCharacterStyle** <br/> |
   
 *Exemplo* 
  
Suponha que a célula Color na primeira linha da seção Character de uma forma esteja definida para esta fórmula:
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Então, se o primeiro caractere do texto da forma for negrito, o texto abrangido pela primeira linha de propriedades da seção Character será azul (4); caso contrário, ele será verde (3). Esse exemplo supõe que as cores padrão estejam sendo usadas.
  
O exemplo a seguir ilustra como definir a célula Style em um programa. A primeira instrução faz referência à célula Style pelo nome, enquanto a segunda instrução faz referência pelo índice. As duas instruções aplicam o estilo itálico ao texto coberto pela segunda linha da seção Character de uma forma.
  

