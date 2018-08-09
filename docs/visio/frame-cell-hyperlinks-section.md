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
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771945"
---
# <a name="frame-cell-hyperlinks-section"></a>Célula Frame (Seção Hyperlinks)

Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Frame pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *nome* . Enquadrar onde Hyperlink.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula Frame pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
| Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkFrame** <br/> |
   

