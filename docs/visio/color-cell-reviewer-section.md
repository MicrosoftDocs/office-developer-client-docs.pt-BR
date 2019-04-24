---
title: Célula Color (Seção Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Um valor RGB que representa a cor atribuída à marcação de um revisor de documento.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341815"
---
# <a name="color-cell-reviewer-section"></a>Célula Color (Seção Reviewer)

Um valor RGB que representa a cor atribuída à marcação de um revisor de documento. 
  
## <a name="remarks"></a>Comentários

As cores são atribuídas aos revisores nesta sequência: vermelho, azul, verde, violeta, laranja, turquesa, cinza. Elas são utilizadas em sequência novamente para os revisores restantes. 
  
Os comentários inseridos na página de desenho original são sempre em amarelo, independente da cor atribuída a um revisor na célula Color. 
  
Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer. Color [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice da linha:  <br/> |**visRowReviewer** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visReviewerColor** <br/> |
   

