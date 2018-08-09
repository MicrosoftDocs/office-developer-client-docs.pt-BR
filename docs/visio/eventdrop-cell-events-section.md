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
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771813"
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
| Índice da linha:  <br/> |**visRowEvent** <br/> |
| Índice da célula:  <br/> |**visEvtCellDrop** <br/> |
   

