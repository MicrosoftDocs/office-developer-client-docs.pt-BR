---
title: Célula AvenueSizeY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Determina a quantidade de espaço vertical entre as formas na página de desenho ao dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Novo Layout de página e, em seguida, clique em mais opções de Layout).
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771291"
---
# <a name="avenuesizey-cell-page-layout-section"></a>Célula AvenueSizeY (Seção Page Layout)

Determina a quantidade de espaço vertical entre as formas na página de desenho ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout** de página e, em seguida, clique em **mais Opções de layout**).
  
## <a name="remarks"></a>Comentários

Também é possível definir esse valor na caixa de diálogo **Espaçamento de Layout e Direcionamento** (na guia **Design**, clique na seta do grupo **Configurar Página**, clique na guia **Layout e Direcionamento** e em **Espaçamento**).
  
A grade dinâmica utilizará a configuração na célula AvenueSizeY somente quando uma forma estiver disponível para o cálculo do espaçamento vertical. Para utilizar a grade dinâmica, na guia **Exibir**, no grupo **Auxílios Visuais**, selecione **Grade Dinâmica**.
  
Para obter uma referência para a célula AvenueSizeY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | AvenueSizeY  <br/> |
   
Para obter uma referência para a célula AvenueSizeY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOAvenueSizeY** <br/> |
   

