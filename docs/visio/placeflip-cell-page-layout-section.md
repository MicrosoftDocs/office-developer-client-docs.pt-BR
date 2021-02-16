---
title: Célula PlaceFlip (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Determina como as formas de colocação são invertidas e/ou giradas em uma página quando a caixa de diálogo Configurar Layout é usada (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434295"
---
# <a name="placeflip-cell-page-layout-section"></a>Célula PlaceFlip (Seção Page Layout)

Determina como as formas de colocação são invertidas e/ou giradas em uma página quando a caixa de diálogo **Configurar Layout** é usada (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Padrão. Não inverter.  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Inverter horizontalmente.  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Inverter verticalmente.  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |Inverter em incrementos de 90 graus.  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |Não inverter.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Comentários

O valor na célula PlaceFlip ajuda a orientar uma forma de colocação em direção à próxima forma de colocação à qual está conectada. É utilizado normalmente ao dispor os desenhos que utilizam a cola estática.
  
Para definir esse comportamento para uma determinada forma, utilize a célula ShapePlaceFlip na seção Page Layout.
  
Para obter uma referência à célula PlaceFlip pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PlaceFlip  <br/> |
   
Para obter uma referência para a célula PlaceFlip pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPageLayout** <br/> |
|Índice de célula:  <br/> |**visPLOPlaceFlip** <br/> |
   

