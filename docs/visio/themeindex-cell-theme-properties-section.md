---
title: Célula ThemeIndex (Seção Theme Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Armazena a enumeração do tema integrado do Microsoft Visio aplicado ao documento, como um inteiro. Quando um novo tema é escolhido para o documento, a célula ThemeIndex do documento e todas as páginas e formas que ele contém é atualizada com o índice do tema integrado.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411908"
---
# <a name="themeindex-cell-theme-properties-section"></a>Célula ThemeIndex (Seção Theme Properties)

Armazena a enumeração do tema integrado do Microsoft Visio aplicado ao documento, como um inteiro. Quando um novo tema é escolhido para o documento, a célula **ThemeIndex** do documento e todas as páginas e formas que ele contém é atualizada com o índice do tema integrado. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ThemeIndex** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ThemeIndex  <br/> |
   
Para fazer referência à célula **ThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowThemeProperties** <br/> |
| Índice de célula:  <br/> |**visThemeIndex** <br/> |
   

