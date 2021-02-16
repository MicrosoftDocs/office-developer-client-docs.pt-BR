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
description: 'Determina a coordenada y do centro de rotação do bloco de texto em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414057"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Célula TxtLocPinY (Seção Text Transform)

Determina a coordenada  *y*  do centro de rotação do bloco de texto em relação à origem do bloco de texto. A fórmula padrão é: 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtLocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtLocPinY  <br/> |
   
Para fazer referência à célula TxtLocPinY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinY** <br/> |
   

