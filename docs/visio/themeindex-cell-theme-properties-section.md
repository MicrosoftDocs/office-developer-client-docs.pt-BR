---
title: Célula ThemeIndex (Seção Theme Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Armazena a enumeração do Microsoft Visio tema interna aplicada ao documento, como um número inteiro. Quando um novo tema é escolhido para o documento, a célula ThemeIndex para o documento e todas as páginas e formas que ele contém é atualizada com o índice do tema interno.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773128"
---
# <a name="themeindex-cell-theme-properties-section"></a>Célula ThemeIndex (Seção Theme Properties)

Armazena a enumeração do Microsoft Visio tema interna aplicada ao documento, como um número inteiro. Quando um novo tema for escolhido para o documento, a célula **ThemeIndex** para o documento e todas as páginas e formas que ele contém é atualizada com o índice do tema interno. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ThemeIndex** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ThemeIndex  <br/> |
   
Para obter uma referência à célula **ThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowThemeProperties** <br/> |
| Índice da célula:  <br/> |**visThemeIndex** <br/> |
   

