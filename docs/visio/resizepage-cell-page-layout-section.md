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
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438089"
---
# <a name="resizepage-cell-page-layout-section"></a>Célula ResizePage (Seção Page Layout)

Determina se a página será ampliada para incluir o desenho após o layout das formas usando a caixa de diálogo Configurar **Layout** (na guia **Design,** no grupo **Layout,** clique em **Re-Layout** page e em Mais Opções de **Layout).**
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Ampliar a página.  <br/> |
| FALSE  <br/> | Não ampliar a página.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula ResizePage pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ResizePage  <br/> |
   
Para obter uma referência à célula ResizePage pelo índice, de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPageLayout** <br/> |
| Índice de célula:  <br/> |**visPLOResizePage** <br/> |
   

