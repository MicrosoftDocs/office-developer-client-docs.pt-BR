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
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385323"
---
# <a name="about-the-formula-tracing-window"></a>Sobre a janela Rastreamento de Fórmula

A janela **Rastreamento de Fórmula** tem como objetivo fornecer aos desenvolvedores de formas informações sobre interdependências entre células — que incluem tanto as células dependentes (células que dependem de uma determinada célula) como as células precedentes (células das quais uma determinada célula depende). 
  
As células em um Microsoft Visio ShapeSheet contêm valores e fórmulas. As fórmulas, por sua vez, podem fazer referências a outras células, permitindo que seja calculado o valor de uma célula com base no valor de outra. No entanto, quando você cria ou mantém formas complexas, a identificação de todas essas interdependências pode se tornar difícil porque uma fórmula pode fazer referência a qualquer célula do desenho, seja ela uma célula do mesmo ShapeSheet ou pertencente a outro objeto do desenho, como uma página, um estilo, um mestre ou outra forma. 
  
A janela **Rastreamento de Fórmula** fornece informações que o ajudam a entender as implicações das alterações que você faz nas células. 
  
## <a name="displaying-the-formula-tracing-window"></a>Mostrar a janela Rastreamento de Fórmula

Para exibir a janela **Rastreamento de Fórmula** com a janela ShapeSheet ativa, em **Ferramentas de ShapeSheet** na guia **Design**, no grupo **Rastreamento de Fórmula**, clique em ** Mostrar Janela**. A janela **Rastreamento de Fórmula** aparece encaixada na janela ShapeSheet por padrão, mas é uma janela ancorada que pode ser encaixada, flutuada ou mesclada com as outras janelas ShapeSheet ancoradas disponíveis, por exemplo, a janela **Explorador de Estilo**. 
  
## <a name="tracing-dependent-cells"></a>Rastreando células dependentes

Para obter uma lista das células dependentes de uma determinada célula, selecione a célula na janela ShapeSheet. Neste exemplo, a célula Width está selecionada. 
  
![Célula de largura está selecionada](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Para exibir as células dependentes, no grupo **Rastreamento de Fórmula**, clique em **Rastrear Dependentes**.
  
Uma lista de todas as células com uma dependência na célula Width é exibida na janela **Rastreamento de Fórmula**. É possível navegar para qualquer célula da lista clicando duas vezes em sua entrada na janela **Rastreamento de Fórmula**. 
  
![Todas as células com uma dependência na célula Largura aparecem na janela Rastreamento de Fórmula](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Rastreando células precedentes

Para obter uma lista das células das quais uma determinada célula é dependente, primeiro selecione a célula na janela ShapeSheet. Neste exemplo, a célula Geometry1.X2 está selecionada. 
  
![A célula Geometry1.X2 está selecionada](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Para exibir suas células precedentes, no grupo **Rastreamento de Fórmula**, clique em **Rastrear Precedentes**.
  
Uma lista de todas as células das quais a célula Geometry1.X2 é dependente aparece na janela **Rastreamento de Fórmula**. Você pode navegar para qualquer célula na lista clicando em sua entrada na janela **Rastreamento de Fórmula**. 
  
![Todas as células das quais a célula Geometry1.X2 depende aparecem na janela Rastreamento de Fórmula](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

