---
title: Sobre a janela Rastreamento de Fórmula
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: A janela Rastreamento de Fórmula tem como objetivo fornecer aos desenvolvedores de formas informações sobre interdependências entre células — que incluem tanto as células dependentes (células que dependem de uma determinada célula) como as células precedentes (células das quais uma determinada célula depende).
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771230"
---
# <a name="about-the-formula-tracing-window"></a>Sobre a janela Rastreamento de Fórmula

A janela **Rastreamento de Fórmula** tem como objetivo fornecer aos desenvolvedores de formas informações sobre interdependências entre células — que incluem tanto as células dependentes (células que dependem de uma determinada célula) como as células precedentes (células das quais uma determinada célula depende). 
  
As células em um Microsoft Visio ShapeSheet contêm valores e fórmulas. Fórmulas podem, por sua vez, têm referências a outras células, permitindo que você para calcular um valor em uma célula com base no valor da célula para outra. Ao criar ou manter formas complexas, no entanto, pode ser difícil identificar todos esses interdependência porque uma fórmula pode fazer referência a qualquer célula no desenho, seja ela uma célula do mesmo ShapeSheet ou uma célula que pertencem a outro objeto no desenho, Por exemplo, uma página, estilo, mestre ou outra forma. 
  
A janela **Rastreamento de fórmula** fornece informações para ajudá-lo a entender as implicações das alterações que você faz nas células. 
  
## <a name="displaying-the-formula-tracing-window"></a>Exibindo a janela rastreamento de fórmula

Para exibir a janela **Rastreamento de fórmula** , com a janela ShapeSheet ativa, em **Ferramentas do ShapeSheet** no * * Design * * guia, no grupo **Rastreamento de fórmula** , clique em **Mostrar janela**. A janela **Rastreamento de fórmula** aparece encaixada na janela ShapeSheet por padrão, mas é uma janela ancorada que pode ser encaixada, flutuada ou mesclada com outras disponíveis janelas ShapeSheet ancoradas, por exemplo, a janela **Gerenciador de estilo** . 
  
## <a name="tracing-dependent-cells"></a>Rastreando células dependentes

Para obter uma lista das células dependentes de uma determinada célula, selecione a célula na janela ShapeSheet. Neste exemplo, a célula Width está selecionada. 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Para exibir as células dependentes, no grupo **Rastreamento de fórmula**, clique em **Rastrear dependentes**.
  
Uma lista de todas as células com uma dependência na célula Width é exibida na janela **Rastreamento de Fórmula**. É possível navegar para qualquer célula da lista clicando duas vezes em sua entrada na janela **Rastreamento de Fórmula**. 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Rastreando células precendent

Para obter uma lista das células das quais uma determinada célula é dependente, primeiro selecione a célula na janela ShapeSheet. Neste exemplo, a célula Geometry1.X2 está selecionada. 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Para exibir suas células precedentes, no grupo **Rastreamento de fórmula**, clique em **Rastrear precedentes**.
  
Uma lista de todas as células que a célula Geometry1. X2 depende é exibida na janela de **Rastreamento de fórmula** . Você pode navegar para qualquer célula na lista clicando duas vezes em sua entrada na janela **Rastreamento de fórmula** . 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

