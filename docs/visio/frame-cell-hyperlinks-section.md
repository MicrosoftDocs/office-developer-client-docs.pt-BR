---
title: Célula Frame (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344846"
---
# <a name="frame-cell-hyperlinks-section"></a>Célula Frame (Seção Hyperlinks)

Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Frame pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *nome* . Quadro onde hiperlink.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula Frame pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
| Índice de linha:  <br/> |**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkFrame** <br/> |
   

