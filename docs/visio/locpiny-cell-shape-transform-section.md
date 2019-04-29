---
title: Célula LocPinY (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Representa a coordenada y do pino da forma (centro de rotação) em relação à origem da forma. A fórmula padrão para determinar a célula LocPinY é:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410592"
---
# <a name="locpiny-cell-shape-transform-section"></a>Célula LocPinY (Seção Shape Transform)

Representa a coordenada *y* do pino da forma (centro de rotação) em relação à origem da forma. A fórmula padrão para determinar a célula LocPinY é: 
  
= Altura \* 0,5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula LocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LocPinY  <br/> |
   
Para fazer referência à célula LocPinY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinY** <br/> |
   

