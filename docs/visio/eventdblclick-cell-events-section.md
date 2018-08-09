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
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771815"
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
   

