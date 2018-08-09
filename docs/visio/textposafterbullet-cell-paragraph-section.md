---
title: Célula TextPosAfterBullet (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Representa a distância entre a primeira linha do parágrafo e o marcador.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773123"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>Célula TextPosAfterBullet (Seção Paragraph)

Representa a distância entre a primeira linha do parágrafo e o marcador. 
  
## <a name="remarks"></a>Comentários

A distância é adicionada à distância contida na célula IndFirst, que é o recuo esquerdo padrão. Esse valor não depende da escala do desenho. 
  
Para fazer referência à célula TextPosAfterBullet pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.TextPosAfterBullet [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula TextPosAfterBullet pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visTextPosAfterBullet** <br/> |
   

