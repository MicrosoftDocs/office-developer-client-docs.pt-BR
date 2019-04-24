---
title: Célula ThemeIndex (seção Theme Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Armazena a enumeração do tema interno do Microsoft Visio aplicado ao documento, como um inteiro. Quando um novo tema é escolhido para o documento, a célula ThemeIndex do documento e todas as páginas e formas que ele contém são atualizadas com o índice do tema interno.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360526"
---
# <a name="themeindex-cell-theme-properties-section"></a>Célula ThemeIndex (seção Theme Properties)

Armazena a enumeração do tema interno do Microsoft Visio aplicado ao documento, como um inteiro. Quando um novo tema é escolhido para o documento, a célula **ThemeIndex** do documento e todas as páginas e formas que ele contém são atualizadas com o índice do tema interno. 
  
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **ThemeIndex** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ThemeIndex  <br/> |
   
Para obter uma referência para a célula **ThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowThemeProperties** <br/> |
| Índice da célula:  <br/> |**visThemeIndex** <br/> |
   

