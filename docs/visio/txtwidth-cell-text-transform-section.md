---
title: Célula TxtWidth (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Determina a largura do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426090"
---
# <a name="txtwidth-cell-text-transform-section"></a>Célula TxtWidth (Seção Text Transform)

Determina a largura do bloco de texto. A fórmula padrão é:
  
= Largura \* 1
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtWidth pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtWidth  <br/> |
   
Para fazer referência à célula TxtWidth pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormWidth** <br/> |
   

