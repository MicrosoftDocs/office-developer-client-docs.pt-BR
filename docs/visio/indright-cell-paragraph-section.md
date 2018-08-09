---
title: Célula IndRight (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem direita do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo direito será o mesmo.
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772072"
---
# <a name="indright-cell-paragraph-section"></a>Célula IndRight (Seção Paragraph)

Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem direita do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo direito será o mesmo.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula IndRight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.IndRight [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula IndRight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visIndentRight** <br/> |
   

