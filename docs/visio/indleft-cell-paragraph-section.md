---
title: Célula IndLeft (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem esquerda do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo esquerdo será o mesmo.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772070"
---
# <a name="indleft-cell-paragraph-section"></a>Célula IndLeft (Seção Paragraph)

Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem esquerda do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo esquerdo será o mesmo.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula IndLeft pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.IndLeft [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula IndLeft pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visIndentLeft** <br/> |
   

