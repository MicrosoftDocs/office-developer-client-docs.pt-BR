---
title: Célula TxtHeight (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Determina a altura do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334388"
---
# <a name="txtheight-cell-text-transform-section"></a>Célula TxtHeight (Seção Text Transform)

Determina a altura do bloco de texto. A fórmula padrão é:
  
= Altura \* 1
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtHeight pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtHeight  <br/> |
   
Para fazer referência à célula TxtHeight pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormHeight** <br/> |
   

