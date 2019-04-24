---
title: Célula LocPinX (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Representa a coordenada x do pino da forma (centro de rotação) em relação à origem da forma. A fórmula padrão para determinar a célula LocPinX é:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358048"
---
# <a name="locpinx-cell-shape-transform-section"></a>Célula LocPinX (Seção Shape Transform)

Representa a coordenada *x* do pino da forma (centro de rotação) em relação à origem da forma. A fórmula padrão para determinar a célula LocPinX é: 
  
= Largura \* 0,5
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula LocPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LocPinX  <br/> |
   
Para fazer referência à célula LocPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinX** <br/> |
   

