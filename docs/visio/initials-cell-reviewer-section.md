---
title: Célula Initials (Seção Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contém as iniciais do revisor de um documento.
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335291"
---
# <a name="initials-cell-reviewer-section"></a>Célula Initials (Seção Reviewer)

Contém as iniciais do revisor de um documento.
  
## <a name="remarks"></a>Comentários

Este valor assume como padrão as iniciais na caixa **iniciais** da guia **geral** da caixa de diálogo opções do **Visio** (clique na guia **arquivo** , em **Opções**e em **geral** ). 
  
Para fazer referência à célula Initials pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer. Initials [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Initials pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice da linha:  <br/> |**visRowReviewer** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visReviewerInitials** <br/> |
   

