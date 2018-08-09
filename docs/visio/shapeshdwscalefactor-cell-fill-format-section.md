---
title: Célula ShapeShdwScaleFactor (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Especifica a porcentagem pela qual a sombra de uma forma pode ser aumentada ou reduzida.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772930"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>Célula ShapeShdwScaleFactor (Seção Fill Format)

Especifica a porcentagem pela qual a sombra de uma forma pode ser aumentada ou reduzida.
  
## <a name="remarks"></a>Comentários

Cada sombra possui um local de pino sombreado, que é um ponto na sombra que corresponde ao pino da forma. Por exemplo, se o pino de uma forma estiver no centro da forma, o local do pino sombreado seria o ponto no centro da sombra. Quando a aplicação da escala em sombras simples, a ampliação é centralizada no local do pino sombreado; Quando a aplicação da escala em sombras oblíquas, ampliação é aplicada na direção oblíqua. 
  
Para definir esse valor para todas as formas de uma página, use a célula ShdwScaleFactor na seção Page Properties.
  
Esse valor corresponde ao valor existente na configuração **Ampliação** na caixa de diálogo **Sombra** (na guia **Página Inicial**, do grupo **Forma**, clique em **Sombra** e em **Opções de sombra**).
  
Para obter uma referência para a célula ShapeShdwScaleFactor pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeShdwScaleFactor  <br/> |
   
Para obter uma referência para a célula ShapeShdwScaleFactor pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillShdwScaleFactor** <br/> |
   

