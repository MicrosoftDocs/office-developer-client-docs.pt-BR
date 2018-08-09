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
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772855"
---
# <a name="selectmode-cell-group-properties-section"></a>Célula SelectMode (Seção Group Properties)

Determina como selecionar uma forma de grupo e seus membros.
  
|**Valor**|**Modo de seleção**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Selecionar somente a forma de grupo.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Selecionar primeiro a forma de grupo.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Selecionar primeiro os membros do grupo.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na caixa de diálogo **comportamento** (com a forma do grupo selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e, em seguida, clique em um modo na lista **seleção** em **grupo Comportamento** ). 
  
Para obter uma referência para a célula SelectMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |SelectMode  <br/> |
   
Para obter uma referência para a célula SelectMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowGroup** <br/> |
|Índice da célula:  <br/> |**visGroupSelectMode** <br/> |
   

