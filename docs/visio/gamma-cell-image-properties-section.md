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
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771948"
---
# <a name="gamma-cell-image-properties-section"></a>Célula Gamma (Seção Image Properties)

Ajusta ou corrige a intensidade de uma imagem para um determinado dispositivo de saída, como um monitor ou scanner. O valor padrão é 1 (sem correção).
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Gamma pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Gamma  <br/> |
   
Para fazer referência à célula Gamma pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageGamma** <br/> |
   

