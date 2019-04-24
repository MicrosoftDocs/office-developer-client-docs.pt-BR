---
title: Célula DisplayMode (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Determina como a forma do grupo e seus membros são exibidos.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332708"
---
# <a name="displaymode-cell-group-properties-section"></a>Célula DisplayMode (Seção Group Properties)

Determina como a forma do grupo e seus membros são exibidos.
  
|**Valor**|**Modo de exibição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Oculta o texto e a forma do grupo.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Exibe a forma do grupo atrás das formas dos membros.  <br/> |**visGrpDispModeBack** <br/> |
|duas  <br/> |Exibe a forma do grupo na frente das formas dos membros.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor selecionando o grupo, clicando em **comportamento** no grupo **design da forma** na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, selecionando um modo de exibição na lista dados do **grupo** . 
  
Para obter uma referência para a célula DisplayMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |DisplayMode  <br/> |
   
Para fazer referência à célula DisplayMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowGroup** <br/> |
|Índice da célula:  <br/> |**visGroupDisplayMode** <br/> |
   

