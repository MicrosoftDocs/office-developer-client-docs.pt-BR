---
title: Célula LockThemeColors (Seção Proteção)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772267"
---
# <a name="lockthemecolors-cell-protection-section"></a>Célula LockThemeColors (Seção Proteção)

Impede a aplicação de cores de tema à forma. 
  
O valor da célula LockThemeColors corresponde à configuração da caixa de seleção **de cores de tema** na caixa de diálogo **proteção** . 
  
Para fazer referência à célula LockThemeColors pelo nome, a partir de outra fórmula ou de um programa, use a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockThemeColors  <br/> |
   
Para fazer referência à célula LockThemeColors pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLock** <br/> |
|Índice da célula:  <br/> |**visLockThemeColors** <br/> |
   

