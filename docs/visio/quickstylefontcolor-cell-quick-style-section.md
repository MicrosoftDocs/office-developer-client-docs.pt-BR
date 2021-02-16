---
title: Célula QuickStyleFontColor (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Determina a cor da fonte dos Estilos Rápidos que o texto de uma forma herda do tema ativo, como um inteiro de 0 a 1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415023"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>Célula QuickStyleFontColor (Seção Quick Style)

Determina a cor da fonte dos Estilos Rápidos que o texto de uma forma herda do tema ativo, como um inteiro de 0 a 1. 
  
|||
|:-----|:-----|
|Valor  <br/> |Descrição  <br/> |
|0  <br/> |O texto da forma usa a cor da fonte Escuro.  <br/> |
|1   <br/> |O texto da forma usa a cor da fonte Light.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **QuickStyleFontColor** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleFontColor  <br/> |
   
Para fazer referência à **célula QuickStyleFontColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de célula:  <br/> |**visQuickStyleFontColor** <br/> |
   

