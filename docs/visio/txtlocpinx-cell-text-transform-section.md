---
title: Célula TxtLocPinX (seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Determina a coordenada x do centro de rotação do bloco de texto em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425852"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Célula TxtLocPinX (seção Text Transform)

Determina a coordenada  *x*  do centro de rotação do bloco de texto em relação à origem do bloco de texto. A fórmula padrão é: 
  
= TxtWidth \* 0,5
  
Essa fórmula avalia o centro horizontal do bloco de texto.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtLocPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtLocPinX  <br/> |
   
Para fazer referência à célula TxtLocPinX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinX** <br/> |
   

