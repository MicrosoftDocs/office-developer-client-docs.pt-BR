---
title: Célula TxtPinY (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Determina a coordenada y do centro de rotação do bloco de texto em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316419"
---
# <a name="txtpiny-cell-text-transform-section"></a>Célula TxtPinY (Seção Text Transform)

Determina a coordenada *y* do centro de rotação do bloco de texto em relação à origem da forma. A fórmula padrão é: 
  
= Altura \* 0,5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtPinY  <br/> |
   
Para fazer referência à célula TxtPinY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormPinY** <br/> |
   

