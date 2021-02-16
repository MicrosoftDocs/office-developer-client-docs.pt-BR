---
title: Célula EventMultiDrop (Seção Eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416717"
---
# <a name="eventmultidrop-cell-events-section"></a>Célula EventMultiDrop (Seção Eventos)

Uma célula de evento que é avaliada quando várias formas são retiradas na página de desenho, como instâncias ou quando as formas são duplicadas ou copiadas.
  
As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.
  
Para referir-se à célula EventMultiDrop pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |EventMultiDrop  <br/> |
   
Para referir-se à célula EventMultiDrop pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowEvent** <br/> |
|Índice de célula:  <br/> |**visEvtCellMultiDrop** <br/> |
   

