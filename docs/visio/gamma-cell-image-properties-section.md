---
title: Célula Gamma (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajusta ou corrige a intensidade de uma imagem para um determinado dispositivo de saída, como um monitor ou scanner. O valor padrão é 1 (sem correção).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315201"
---
# <a name="gamma-cell-image-properties-section"></a>Célula Gamma (Seção Image Properties)

Ajusta ou corrige a intensidade de uma imagem para um determinado dispositivo de saída, como um monitor ou scanner. O valor padrão é 1 (sem correção).
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Gamma pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Gama  <br/> |
   
Para fazer referência à célula Gamma pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageGamma** <br/> |
   

