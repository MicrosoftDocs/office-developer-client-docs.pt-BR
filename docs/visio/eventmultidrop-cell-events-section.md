---
title: Célula EventMultiDrop (Seção Eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771830"
---
# <a name="eventmultidrop-cell-events-section"></a>Célula EventMultiDrop (Seção Eventos)

Uma célula de evento que é avaliada quando várias formas são colocadas na página de desenho, como instâncias ou quando as formas são duplicar ou colar.
  
As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.
  
Para fazer referência à célula EventMultiDrop pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |EventMultiDrop  <br/> |
   
Para fazer referência à célula EventMultiDrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowEvent** <br/> |
|Índice da célula:  <br/> |**visEvtCellMultiDrop** <br/> |
   

