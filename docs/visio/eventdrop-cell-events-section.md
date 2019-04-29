---
title: Célula EventDrop (Seção Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Uma célula de evento avaliada ao soltar uma forma na página de desenho, como uma instância ou ao duplicar ou colar uma forma.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408590"
---
# <a name="eventdrop-cell-events-section"></a>Célula EventDrop (Seção Events)

Uma célula de evento avaliada ao soltar uma forma na página de desenho, como uma instância ou ao duplicar ou colar uma forma.
  
## <a name="remarks"></a>Comentários

As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.
  
Para fazer referência à célula EventDrop pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | EventDrop  <br/> |
   
Para fazer referência à célula EventDrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowEvent** <br/> |
| Índice da célula:  <br/> |**visEvtCellDrop** <br/> |
   

