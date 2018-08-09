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
description: 'Representa o y-coordenadas do pino da forma (Centro de rotação) em relação à origem da forma. A fórmula padrão para determinar LocPinY é:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772281"
---
# <a name="locpiny-cell-shape-transform-section"></a>Célula LocPinY (Seção Shape Transform)

Representa o *y* -coordenadas do pino da forma (Centro de rotação) em relação à origem da forma. A fórmula padrão para determinar LocPinY é: 
  
= A altura \* 0.5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula LocPinY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LocPinY  <br/> |
   
Para fazer referência à célula LocPinY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinY** <br/> |
   

