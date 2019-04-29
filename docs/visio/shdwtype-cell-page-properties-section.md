---
title: Célula ShdwType (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indica o tipo de sombra padrão para uma página.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424095"
---
# <a name="shdwtype-cell-page-properties-section"></a>Célula ShdwType (Seção Page Properties)

Indica o tipo de sombra padrão para uma página.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 1  <br/> | Simples  <br/> |**visFSTSimple** <br/> |
| duas  <br/> | Oblíqua  <br/> |**visFSTOblique** <br/> |
|3D  <br/> |Inner  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Comentários

 O tipo de sombra descrito nesta célula é usado sempre que a célula ShapeShdwType (o tipo de sombra para uma forma individual na página) é definida como padrão da página (**visFSTPageDefault** ). 
  
Os tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI). Uma sombra simples dá o efeito na forma sendo sombreada em um plano paralelo localizado um pouco atrás dela. As sombras oblíquas são descritas como tal na UI e apresentam o efeito de uma sombra sendo moldada em um plano perpendicular à forma. 
  
Para obter uma lista de tipos de sombra simples e oblíquas, consulte a lista **Estilo**, na guia **Sombras** da caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta **Configurar Página**). 
  
Para obter uma referência para a célula ShdwType pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwType  <br/> |
   
Para obter uma referência para a célula ShapeShdwOffsetX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageShdwType** <br/> |
   

