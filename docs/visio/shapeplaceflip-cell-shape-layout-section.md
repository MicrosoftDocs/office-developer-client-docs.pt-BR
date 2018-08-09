---
title: Célula ShapePlaceFlip (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Determina como as formas de colocação são invertidas, giradas, ou ambos, na página ao dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772894"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>Célula ShapePlaceFlip (Seção Shape Layout)

Determina como as formas de colocação são invertidas, giradas, ou ambos, na página ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Utilizar padrão de página.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Inverter horizontalmente.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Inverter verticalmente.  <br/> |**visLOFlipY** <br/> |
|4  <br/> |Inverter em incrementos de 90 graus entre 0 e 270.  <br/> |**visLOFlipRotate** <br/> |
|8  <br/> |Não inverter.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Comentários

O valor na célula ShapePlaceFlip ajuda a orientar uma forma de colocação em direção à próxima forma de colocação à qual está conectada.
  
Para definir esse comportamento para *todas* as formas na página de desenho, use a célula PlaceFlip na seção Page Layout. 
  
Para obter uma referência para a célula ShapePlaceFlip pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePlaceFlip  <br/> |
   
Para obter uma referência para a célula ShapePlaceFlip pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOPlaceFlip** <br/> |
   

