---
title: Célula NewWindow (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Especifica quando abrir o hiperlink em uma nova janela.
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772411"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Célula NewWindow (Seção Hyperlinks)

Especifica quando abrir o hiperlink em uma nova janela.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Abrir o documento, o site da Web ou a página vinculada em uma nova janela.  <br/> |
| FALSO  <br/> | Padrão. Não abrir uma nova janela para o hiperlink.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula NewWindow pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *Nome* . NewWindow onde Hyperlink.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula NewWindow pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
| Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2,...  <br/> |
| Índice da célula:  <br/> |**visHLinkNewWin** <br/> |
   

