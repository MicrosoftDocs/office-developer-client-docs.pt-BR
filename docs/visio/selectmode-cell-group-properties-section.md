---
title: Célula SelectMode (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Determina como selecionar uma forma de grupo e seus membros.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435359"
---
# <a name="selectmode-cell-group-properties-section"></a>Célula SelectMode (Seção Group Properties)

Determina como selecionar uma forma de grupo e seus membros.
  
|**Valor**|**Modo de seleção**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Selecionar somente a forma de grupo.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1   <br/> |Selecionar primeiro a forma de grupo.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2   <br/> |Selecionar primeiro os membros do grupo.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na caixa de diálogo Comportamento (com a forma de grupo selecionada, na guia  Desenvolvedor, no grupo **Design** da Forma, clique em Comportamento e em um modo na lista Seleção em Comportamento do **Grupo).**  [](run-in-developer-mode-display-the-developer-tab.md) 
  
Para obter uma referência para a célula SelectMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |SelectMode  <br/> |
   
Para obter uma referência para a célula SelectMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowGroup** <br/> |
|Índice de célula:  <br/> |**visGroupSelectMode** <br/> |
   

