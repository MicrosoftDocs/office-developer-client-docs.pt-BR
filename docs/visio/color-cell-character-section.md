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
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771499"
---
# <a name="color-cell-character-section"></a>Célula Color (Seção Character)

Determina a cor utilizada no texto da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
Para inserir uma cor personalizada, use a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet. Quando usado em operações numéricas, as cores têm valores de 24 e acima. 
  
É possível definir a transparência da cor do texto na célula Transparency.
  
Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.Color [ *i* ] onde *i* = < 1 >, 2, 3,...  <br/> |
   
Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visCharacterColor** <br/> |
   

