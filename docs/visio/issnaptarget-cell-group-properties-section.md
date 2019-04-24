---
title: Célula IsSnapTarget (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Determina o ajuste a um grupo ou a formas no grupo.
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317896"
---
# <a name="issnaptarget-cell-group-properties-section"></a>Célula IsSnapTarget (Seção Group Properties)

Determina o ajuste a um grupo ou a formas no grupo.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |Permite ajustar a formas no grupo.  <br/> |
|FALSE  <br/> |Permite ajustar somente ao grupo.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor selecionando o grupo, clicando em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Ajustar às formas do membro**. 
  
Para obter uma referência para a célula IsSnapTarget pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |IsSnapTarget  <br/> |
   
Para obter uma referência para a célula IsSnapTarget pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowGroup** <br/> |
|Índice da célula:  <br/> |**visGroupIsSnapTarget** <br/> |
   

