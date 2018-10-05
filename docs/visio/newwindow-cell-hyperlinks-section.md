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
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396334"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Célula NewWindow (Seção Hyperlinks)

Especifica quando abrir o hiperlink em uma nova janela.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | Abra a página vinculada, documento ou site em uma nova janela.  <br/> |
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
   

