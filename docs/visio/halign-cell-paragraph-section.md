---
title: Célula HAlign (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Determina o alinhamento horizontal do texto no bloco de texto da forma.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414736"
---
# <a name="halign-cell-paragraph-section"></a>Célula HAlign (Seção Paragraph)

Determina o alinhamento horizontal do texto no bloco de texto da forma.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Alinhar à esquerda  <br/> |**visHorzLeft** <br/> |
| 1   <br/> | Centro  <br/> |**visHorzCenter** <br/> |
| 2   <br/> | Alinhar à direita  <br/> |**visHorzRight** <br/> |
| 3   <br/> | Justificar  <br/> |**visHorzJustify** <br/> |
| 4   <br/> | Forçar justificado  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Comentários

A opção Justificar adiciona espaço entre as palavras em todas as linhas, com exceção da última linha do parágrafo, para alinhar os lados esquerdo e direito do texto com as margens.
  
A opção Forçar justificado alinha todas as linhas no parágrafo, inclusive a última.
  
Para fazer referência à célula HAlign pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.HorzAlign[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula HAlign pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice de linha:  <br/> |**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHorzAlign** <br/> |
   

