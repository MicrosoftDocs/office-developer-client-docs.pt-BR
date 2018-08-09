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
description: 'Determina a y-coordenadas do centro do bloco de texto de rotação em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773199"
---
# <a name="txtpiny-cell-text-transform-section"></a>Célula TxtPinY (Seção Text Transform)

Determina a *y* -coordenadas do centro do bloco de texto de rotação em relação à origem da forma. A fórmula padrão é: 
  
= A altura \* 0.5
  
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
   

