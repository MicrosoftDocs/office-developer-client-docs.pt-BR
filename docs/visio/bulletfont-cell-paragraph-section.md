---
title: Célula BulletFont (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Representa o número da fonte usada para formatar o texto quando uma sequência de caracteres com marcadores personalizada for especificada e o valor da célula Bullet for diferente de zero.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438460"
---
# <a name="bulletfont-cell-paragraph-section"></a>Célula BulletFont (Seção Paragraph)

Representa o número da fonte usada para formatar o texto quando uma sequência de caracteres com marcadores personalizada for especificada e o valor da célula Bullet for diferente de zero. 
  
## <a name="remarks"></a>Comentários

Os números de fonte variam de acordo com as fontes instaladas em seu sistema. Se o valor for 0 e houver uma sequência de caracteres com marcadores personalizada, a fonte usada será a mesma do primeiro caractere do parágrafo.
  
Para fazer referência à célula BulletFont pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.BulletFont[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula BulletFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice de linha:  <br/> |**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visBulletFont** <br/> |
   

