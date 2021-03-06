---
title: Célula BeginArrowSize (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Determina o tamanho da ponta de seta no início da linha.
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412279"
---
# <a name="beginarrowsize-cell-line-format-section"></a>Célula BeginArrowSize (Seção Line Format)

Determina o tamanho da ponta de seta no início da linha.
  
|**Valor**|**Tamanho**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Muito pequeno  <br/> |**visArrowSizeVerySmall** <br/> |
| 1   <br/> | Pequeno  <br/> |**visArrowSizeSmall** <br/> |
| 2   <br/> | Média  <br/> |**visArrowSizeMedium** <br/> |
| 3   <br/> | Grande  <br/> |**visArrowSizeLarge** <br/> |
| 4   <br/> | Muito grande  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5   <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | PauloA  <br/> |**visArrowSizeColssal** <br/> |
   
## <a name="remarks"></a>Comentários

É possível também definir o tamanho da ponta de seta na caixa de diálogo **Linha**. 
  
Para fazer referência à célula BeginArrowSize pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BeginArrowSize  <br/> |
   
Para fazer referência à célula BeginArrowSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLine** <br/> |
| Índice de célula:  <br/> |**visLineBeginArrowSize** <br/> |
   

