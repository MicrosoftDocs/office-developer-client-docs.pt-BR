---
title: Célula SpBefore (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425754"
---
# <a name="spbefore-cell-paragraph-section"></a>Célula SpBefore (Seção Paragraph)

Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.
  
## <a name="remarks"></a>Comentários

Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço anterior será a mesma.
  
Para fazer referência à célula SpBefore pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.SpBefore[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula SpBefore pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice de linha:  <br/> |**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSpaceBefore** <br/> |
   

