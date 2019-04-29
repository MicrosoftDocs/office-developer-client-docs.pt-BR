---
title: Célula Prompt (Seção User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Especifica um comentário ou prompt descritivo para a célula definida pelo usuário. O aplicativo inclui automaticamente o texto do prompt entre aspas () para indicar que se trata de uma cadeia de caracteres de texto. Se você digitar um sinal de igual (=) e omitir as aspas, é possível inserir uma fórmula na célula avaliada pelo aplicativo.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435723"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Célula Prompt (Seção User-Defined Cells)

Especifica um comentário ou prompt descritivo para a célula definida pelo usuário. O aplicativo automaticamente inclui o texto do prompt entre aspas (" ") para indicar que é uma sequência de texto. Se você digitar um sinal de igual (=) e omitir as aspas, é possível inserir uma fórmula na célula avaliada pelo aplicativo.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Utilizador.  *Nome* . Avisar onde usuário.  *Name*  é o nome da linha  <br/> |
   
Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionUser** <br/> |
| Índice de linha:  <br/> |**visRowUser +** *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visUserPrompt** <br/> |
   

