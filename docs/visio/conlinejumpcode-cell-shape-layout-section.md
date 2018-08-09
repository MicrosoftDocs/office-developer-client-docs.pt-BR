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
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771581"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Célula ConLineJumpCode (Seção Shape Layout)

Determina quando um conector salta.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |
          Como especificado na página, no menu **Design**, clique na seta do grupo **Configurar Página** e na guia **Layout e Direcionamento** para ver as especificações da página.
  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nunca  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Sempre  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Outro conector salta  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |
          Nenhum conector salta
  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Comentários

Você pode também definir o valor desta célula selecionando um conector dinâmico, clicando em **comportamento** , no grupo **Design** da forma na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **conector** . 
  
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
   

