---
title: Célula BulletSize (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Especifica o tamanho de um marcador.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405419"
---
# <a name="bulletsize-cell-paragraph-section"></a>Célula BulletSize (Seção Paragraph)

Especifica o tamanho de um marcador. 
  
## <a name="remarks"></a>Comentários

Esse valor pode ser especificado para marcadores predefinidos ou personalizados, como um valor percentual ou específico. 
  
Se o valor for zero (0), o marcador será do mesmo tamanho de fonte do primeiro caractere do parágrafo. Se o valor for percentual, o tamanho do marcador será um percentual do tamanho da fonte do primeiro caractere do parágrafo. Números negativos são tratados como percentuais.
  
Para fazer referência à célula BulletSize pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.BulletFontSize[  *i*  ] onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula BulletSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice de linha:  <br/> |**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visBulletFontSize** <br/> |
   

