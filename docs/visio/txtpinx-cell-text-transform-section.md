---
title: Célula TxtPinX (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina a coordenada x do centro de rotação do bloco de texto em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423493"
---
# <a name="txtpinx-cell-text-transform-section"></a>Célula TxtPinX (Seção Text Transform)

Determina a coordenada *x* do centro de rotação do bloco de texto em relação à origem da forma. A fórmula padrão é: 
  
= Largura \* 0,5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula TxtPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtPinX  <br/> |
   
Para fazer referência à célula TxtPinX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormPinX** <br/> |
   

