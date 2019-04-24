---
title: Célula EventDblClick (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Uma célula de evento avaliada ao se clicar duas vezes em uma forma.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337167"
---
# <a name="eventdblclick-cell-events-section"></a>Célula EventDblClick (Seção Events)

Uma célula de evento avaliada ao se clicar duas vezes em uma forma.
  
## <a name="remarks"></a>Comentários

As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.
  
Para fazer referência à célula EventDblClick pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | EventDblClick  <br/> |
   
Para fazer referência à célula EventDblClick pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowEvent** <br/> |
| Índice da célula:  <br/> |**visEvtCellDblClick** <br/> |
   

