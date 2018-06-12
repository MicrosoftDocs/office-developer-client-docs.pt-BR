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
description: 'Representa o x-coordenadas do pino da forma (Centro de rotação) em relação à origem da forma. A fórmula padrão para determinar LocPinX é:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772294"
---
# <a name="locpinx-cell-shape-transform-section"></a>Célula LocPinX (Seção Shape Transform)

Representa o *x* -coordenadas do pino da forma (Centro de rotação) em relação à origem da forma. A fórmula padrão para determinar LocPinX é: 
  
= A largura \* 0.5
  
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula LocPinX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LocPinX  <br/> |
   
Para obter uma referência à célula LocPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormLocPinX** <br/> |
   

