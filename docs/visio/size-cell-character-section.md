---
title: Célula Size (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Determina o tamanho do texto no bloco de texto da forma.
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415597"
---
# <a name="size-cell-character-section"></a>Célula Size (Seção Character)

Determina o tamanho do texto no bloco de texto da forma.
  
## <a name="remarks"></a>Comentários

O tamanho do texto não depende da escala do desenho. Se o desenho estiver em escala, o tamanho do texto será o mesmo.
  
Para fazer referência à célula Size pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.Size[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula Size pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice de linha:  <br/> |**visRowCharacter** +  *i*            onde  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCharacterSize** <br/> |
   

