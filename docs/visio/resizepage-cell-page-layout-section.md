---
title: Célula ResizePage (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Determina se a página de ser ampliada para incluir o desenho depois que as formas são dispostas usando a caixa de diálogo Configurar Layout (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772722"
---
# <a name="resizepage-cell-page-layout-section"></a>Célula ResizePage (Seção Page Layout)

Determina se é necessário ampliar a página para incluir o desenho após dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout** de página e, em seguida, clique em **mais Layout Opções de**).
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Ampliar a página.  <br/> |
| FALSO  <br/> | Não ampliar a página.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula ResizePage pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ResizePage  <br/> |
   
Para obter uma referência à célula ResizePage pelo índice, de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOResizePage** <br/> |
   

