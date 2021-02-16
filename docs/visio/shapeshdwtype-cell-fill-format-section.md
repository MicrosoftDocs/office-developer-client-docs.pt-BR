---
title: Célula ShapeShdwType (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Especifica o tipo de sombra para uma forma.
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430256"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Célula ShapeShdwType (Seção Fill Format)

Especifica o tipo de sombra para uma forma. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Usar página padrão (padrão)  <br/> |**visFSTPageDefault** <br/> |
|1   <br/> |Simples  <br/> |**visFSTSimple** <br/> |
|2   <br/> |Oblíqua  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Comentários

Use esta célula para aplicar uma sombra de forma diferente do padrão de página (o tipo de sombra padrão da página é definido na célula ShdwType na seção Page Properties).
  
Os tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI). Uma sombra simples dá o efeito na forma sendo sombreada em um plano paralelo localizado atrás dela. As sombras oblíquas são descritas como tal na UI e apresentam o efeito de uma sombra sendo moldada em um plano perpendicular à forma. 
  
Para obter uma lista de tipos de sombra simples e oblíquas, consulte a caixa **Estilo**, na caixa de diálogo **Sombra** (na guia **Página Inicial**, do grupo **Forma**, clique em **Sombra** e em **Opções de Sombra**).
  
Para obter uma referência para a célula ShapeShdwType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeShdwType  <br/> |
   
Para obter uma referência para a célula ShapeShdwType pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowFill** <br/> |
|Índice de célula:  <br/> |**visFillShdwType** <br/> |
   

