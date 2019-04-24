---
title: Célula Scale (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Controla a largura da fonte. O valor padrão para esta célula é 100%.
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341626"
---
# <a name="scale-cell-character-section"></a>Célula Scale (Seção Character)

Controla a largura da fonte. O valor padrão para esta célula é 100%.
  
## <a name="remarks"></a>Comentários

Defina a porcentagem entre 1% e 99% para diminuir a largura da fonte e entre 101% e 600% para aumentar a largura da fonte.
  
Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**). 
  
Para obter uma referência para a célula Scale pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char. FontScale [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Scale pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterFontScale** <br/> |
   

