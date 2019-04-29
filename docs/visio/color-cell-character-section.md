---
title: Célula Color (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Determina a cor utilizada no texto da forma.
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439986"
---
# <a name="color-cell-character-section"></a>Célula Color (Seção Character)

Determina a cor utilizada no texto da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é sua cor RGB e RGB ( *r, g, b*), e não um número, serão mostrados na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24. 
  
É possível definir a transparência da cor do texto na célula Transparency.
  
Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char. Color [ *i* ] onde *i* = <1>, 2, 3,...  <br/> |
   
Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice de linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visCharacterColor** <br/> |
   

