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
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773061"
---
# <a name="style-cell-character-section"></a>Célula Style (Seção Character)

Mostra a formatação de caracteres aplicada a um intervalo de texto no bloco de texto da forma.
  
|**Style**|**Valor**|**Constante de automação**|
|:-----|:-----|:-----|
| Negrito  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Itálico  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Sublinhado  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Caixa alta  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>Comentários

A célula Style conterá informações de formatação aplicada a um subintervalo de texto de uma forma se a seção Characters contiver diversas linhas. Caso contrário, ela conterá informações de formatação para todo o texto da forma.
  
O valor representa um número binário em que cada bit indica um estilo de caractere. Por exemplo, um valor de 3 representa o texto formatado em itálico e negrito. Se o valor do estilo for 0, o texto é simples ou não formatado. Você pode testar para um determinado formato utilizando Boolean BIT\* funções. Consulte a documentação de programação para obter detalhes sobre essas funções.
  
Para fazer referência à célula Style pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.Style [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Style pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCharacterStyle** <br/> |
   
 *Exemplo* 
  
Suponha que a célula Color na primeira linha da seção Character de uma forma esteja definida para esta fórmula:
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Então, se o primeiro caractere do texto da forma for negrito, o texto abrangido pela primeira linha de propriedades da seção Character será azul (4); caso contrário, ele será verde (3). Esse exemplo supõe que as cores padrão estejam sendo usadas.
  
O exemplo a seguir ilustra como definir a célula Style em um programa. A primeira instrução faz referência à célula Style pelo nome, enquanto a segunda instrução faz referência pelo índice. As duas instruções aplicam o estilo itálico ao texto coberto pela segunda linha da seção Character de uma forma.
  

