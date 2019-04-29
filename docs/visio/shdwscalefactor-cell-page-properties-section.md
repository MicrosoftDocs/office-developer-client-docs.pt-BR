---
title: Célula ShdwScaleFactor (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Especifica a porcentagem de aumento ou redução da sombra de uma forma.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429002"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Célula ShdwScaleFactor (Seção Page Properties)

Especifica a porcentagem de aumento ou redução da sombra de uma forma. 
  
## <a name="remarks"></a>Comentários

Cada sombra possui um local de pino sombreado, que representa um ponto na sombra que corresponde ao pino da forma. Por exemplo, se o pino de uma forma estiver no centro dela, então o local do pino sombreado será o ponto no centro da sombra. Ao aplicar escala a sombras simples, a ampliação é centralizada no local de PIN sombreado; ao aplicar escala a sombras oblíquas, a ampliação é aplicada na direção oblíqua. 
  
 Essa porcentagem é usada quando o tipo de sombra de uma forma está definido como padrão da página (célula ShapeShdwType equivale a * * visFSTPageDefault * *). 
  
Para configurar este comportamento para uma forma individual, use a célula ShapeShdwScaleFactor na seção Fill Format.
  
Este valor corresponde àquele existente na caixa **Ampliação** da guia **Sombras** da caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta  **Configurar Página**). 
  
Para obter uma referência para a célula ShdwScaleFactor pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwScaleFactor  <br/> |
   
Para obter uma referência para a célula ShdwScaleFactor pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageShdwScaleFactor** <br/> |
   

