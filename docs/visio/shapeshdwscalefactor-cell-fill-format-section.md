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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436262"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>Célula ShapeShdwScaleFactor (Seção Fill Format)

Especifica a porcentagem pela qual a sombra de uma forma pode ser aumentada ou reduzida.
  
## <a name="remarks"></a>Comentários

Cada sombra possui um local de pino sombreado, que representa um ponto na sombra que corresponde ao pino da forma. Por exemplo, se o pino de uma forma estiver no centro dela, então o local do pino sombreado será o ponto no centro da sombra. Ao aplicar escala a sombras simples, a ampliação é centralizada no local de PIN sombreado; ao aplicar escala a sombras oblíquas, a ampliação é aplicada na direção oblíqua. 
  
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
|Índice de linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillShdwScaleFactor** <br/> |
   

