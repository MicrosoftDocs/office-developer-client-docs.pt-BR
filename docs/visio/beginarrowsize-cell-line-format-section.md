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
ms.openlocfilehash: b38e4a0685fce6d7f4aea2192ed123665eacf40a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771288"
---
# <a name="beginarrowsize-cell-line-format-section"></a>Célula BeginArrowSize (Seção Line Format)

Determina o tamanho da ponta de seta no início da linha.
  
|**Valor**|**Size**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Muito pequeno  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | Pequeno  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | Médio  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | Grande  <br/> |**visArrowSizeLarge** <br/> |
| 4  <br/> | Muito grande  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5  <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6  <br/> | Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Coment�rios

Você também pode definir o tamanho da ponta de seta na caixa de diálogo **linha** . 
  
Para obter uma referência à célula BeginArrowSize pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BeginArrowSize  <br/> |
   
Para obter uma referência à célula BeginArrowSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLine** <br/> |
| Índice da célula:  <br/> |**visLineBeginArrowSize** <br/> |
   

