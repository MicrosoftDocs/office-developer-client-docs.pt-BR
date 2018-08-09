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
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773042"
---
# <a name="spbefore-cell-paragraph-section"></a>Célula SpBefore (Seção Paragraph)

Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.
  
## <a name="remarks"></a>Comentários

Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço anterior será a mesma.
  
Para fazer referência à célula SpBefore pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.SpBefore [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula SpBefore pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSpaceBefore** <br/> |
   

