---
title: Célula TxtLocPinY (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Determina a y-coordenadas do centro do bloco de texto de rotação em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773191"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Célula TxtLocPinY (Seção Text Transform)

Determina a *y* -coordenadas do centro do bloco de texto de rotação em relação à origem do bloco de texto. A fórmula padrão é: 
  
= TxtHeight \* 0.5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtLocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtLocPinY  <br/> |
   
Para fazer referência à célula TxtLocPinY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinY** <br/> |
   

