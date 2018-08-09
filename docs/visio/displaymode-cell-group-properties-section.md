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
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771723"
---
# <a name="displaymode-cell-group-properties-section"></a>Célula DisplayMode (Seção Group Properties)

Determina como a forma do grupo e seus membros são exibidos.
  
|**Valor**|**Modo de exibição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Oculta o texto e a forma do grupo.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Exibe a forma do grupo atrás das formas dos membros.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Exibe a forma do grupo na frente das formas dos membros.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Comentários

Você pode também definir esse valor selecionando o grupo, clicando em **comportamento** , no grupo **Design** da forma na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, selecionando um modo de exibição da lista de **dados de grupo** . 
  
Para obter uma referência para a célula DisplayMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |DisplayMode  <br/> |
   
Para obter uma referência para a célula DisplayMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowGroup** <br/> |
|Índice da célula:  <br/> |**visGroupDisplayMode** <br/> |
   

