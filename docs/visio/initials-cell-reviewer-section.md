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
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772088"
---
# <a name="initials-cell-reviewer-section"></a>Célula Initials (Seção Reviewer)

Contém as iniciais do revisor de um documento.
  
## <a name="remarks"></a>Comentários

Esse valor utiliza como padrão as iniciais na caixa **iniciais** , na guia **Geral** na caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , clique em **Opções**e, em seguida, clique em **Geral** ). 
  
Para fazer referência à célula Initials pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer. Initials [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Initials pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice da linha:  <br/> |**visRowReviewer** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visReviewerInitials** <br/> |
   

