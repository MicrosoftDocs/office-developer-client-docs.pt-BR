---
title: Célula QuickStyleFontColor (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Determina a cor da fonte dos estilos rápidos que um texto de forma herda o tema ativo, como um inteiro de 0-1.
ms.openlocfilehash: 8f2d77508dccffccf472f8ab80517e840f860541
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772624"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>Célula QuickStyleFontColor (Seção Quick Style)

Determina a cor da fonte dos estilos rápidos que um texto de forma herda o tema ativo, como um inteiro de 0-1. 
  
|||
|:-----|:-----|
|Value  <br/> |Descrição  <br/> |
|0  <br/> |O texto de forma usa a cor de fonte escura.  <br/> |
|1  <br/> |O texto de forma usa a cor da fonte claro.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **QuickStyleFontColor** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleFontColor  <br/> |
   
Para obter uma referência à célula **QuickStyleFontColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice da célula:  <br/> |**visQuickStyleFontColor** <br/> |
   

