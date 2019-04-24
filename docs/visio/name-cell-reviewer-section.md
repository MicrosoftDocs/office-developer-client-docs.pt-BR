---
title: Célula Name (Seção Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Contém o nome do revisor de um documento.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335165"
---
# <a name="name-cell-reviewer-section"></a>Célula Name (Seção Reviewer)

Contém o nome do revisor de um documento.
  
## <a name="remarks"></a>Comentários

 Este valor padrão é o nome encontrado na caixa **nome de usuário** na guia **geral** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , em **Opções**e em **geral**). 
  
Para fazer referência à célula Name pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer.Name [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Name pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice da linha:  <br/> |**visRowReviewer** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visReviewerName** <br/> |
   

