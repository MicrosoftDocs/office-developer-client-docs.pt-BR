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
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772910"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Célula ShapeShdwType (Seção Fill Format)

Especifica o tipo de sombra para uma forma. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Usar página padrão (padrão)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Simples  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Oblíquo  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Comentários

Use esta célula para aplicar a sombra de uma forma que seja diferente da página padrão (o tipo de sombra de padrão de página é definido na célula ShdwType na seção Page Properties).
  
Tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI). Uma sombra simples dá o efeito da forma sendo sombreada em um plano paralelo localizado por trás da forma. Sombras oblíquas são descritas como sombras oblíquas na interface de usuário e fornecer o efeito de uma sombra sendo convertida em um plano perpendicular à forma. 
  
Para obter uma lista de tipos de sombra simples e oblíquas, consulte a caixa **Estilo**, na caixa de diálogo **Sombra** (na guia **Página Inicial**, do grupo **Forma**, clique em **Sombra** e em **Opções de Sombra**).
  
Para obter uma referência para a célula ShapeShdwType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeShdwType  <br/> |
   
Para obter uma referência para a célula ShapeShdwType pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillShdwType** <br/> |
   

