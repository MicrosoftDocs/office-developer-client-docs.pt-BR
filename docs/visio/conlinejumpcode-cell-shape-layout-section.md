---
title: Célula ConLineJumpCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Determina quando um conector salta.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284085"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Célula ConLineJumpCode (Seção Shape Layout)

Determina quando um conector salta.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Como especificado na página, no menu **Design**, clique na seta do grupo **Configurar Página** e na guia **Layout e Direcionamento** para ver as especificações da página.  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nunca  <br/> |**visSLOJumpNever** <br/> |
|duas  <br/> |Sempre  <br/> |**visSLOJumpAlways** <br/> |
|3D  <br/> |Outro conector salta  <br/> |**visSLOJumpOther** <br/> |
|quatro  <br/> |Nenhum conector salta  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula selecionando um conector dinâmico, clicando em **comportamento** no grupo **design da forma** na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **conector** . 
  
Para obter uma referência para a célula ConLineJumpCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ConLineJumpCode  <br/> |
   
Para obter uma referência para a célula ConLineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOJumpCode** <br/> |
   

