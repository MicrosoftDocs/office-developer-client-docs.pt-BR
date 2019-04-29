---
title: Célula IndFirst (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Representa a distância do recuo da primeira linha de cada parágrafo no bloco de texto da forma em relação ao recuo esquerdo do parágrafo. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo da primeira linha será o mesmo.
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410319"
---
# <a name="indfirst-cell-paragraph-section"></a>Célula IndFirst (Seção Paragraph)

Representa a distância do recuo da primeira linha de cada parágrafo no bloco de texto da forma em relação ao recuo esquerdo do parágrafo. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo da primeira linha será o mesmo.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula IndFirst pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para. IndFirst [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula IndFirst pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice de linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visIndentFirst** <br/> |
   

