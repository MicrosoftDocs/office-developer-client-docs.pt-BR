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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411502"
---
# <a name="initials-cell-reviewer-section"></a>Célula Initials (Seção Reviewer)

Contém as iniciais do revisor de um documento.
  
## <a name="remarks"></a>Comentários

Esse valor assume como padrão as iniciais  na caixa Iniciais da guia Geral  da caixa de diálogo Opções do **Visio** (clique na guia Arquivo, em Opções e em  **Geral).** 
  
Para fazer referência à célula Initials pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer.Initials [  *i*  ] onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Initials pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice de linha:  <br/> |**visRowReviewer**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visReviewerInitials** <br/> |
   

