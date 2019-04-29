---
title: Célula EndArrowSize (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Determina o tamanho da ponta de seta no final da linha.
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438075"
---
# <a name="endarrowsize-cell-line-format-section"></a>Célula EndArrowSize (Seção Line Format)

Determina o tamanho da ponta de seta no final da linha.
  
|**Valor**|**Tamanho**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Muito pequeno  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Pequeno  <br/> |**visArrowSizeSmall** <br/> |
|duas  <br/> |Média  <br/> |**visArrowSizeMedium** <br/> |
|3D  <br/> |Grande  <br/> |**visArrowSizeLarge** <br/> |
|4   <br/> |Extra grande  <br/> |**visArrowSizeVeryLarge** <br/> |
|5   <br/> |Empréstimo  <br/> |**visArrowSizeJumbo** <br/> |
|6   <br/> |Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**).
  
Para obter uma referência para a célula EndArrowSize pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |EndArrowSize  <br/> |
   
Para obter uma referência à célula EndArrowSize pelo índice, de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLine** <br/> |
|Índice de célula:  <br/> |**visLineEndArrowSize** <br/> |
   

