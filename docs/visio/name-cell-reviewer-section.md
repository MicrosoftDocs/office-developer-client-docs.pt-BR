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
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772409"
---
# <a name="name-cell-reviewer-section"></a>Célula Name (Seção Reviewer)

Contém o nome do revisor de um documento.
  
## <a name="remarks"></a>Comentários

 O valor padrão é o nome encontrado na caixa **nome** do usuário na guia **Geral** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , clique em **Opções**e, em seguida, clique em **Geral**). 
  
Para obter uma referência à célula Name pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer.Name [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Name pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice da linha:  <br/> |**visRowReviewer** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visReviewerName** <br/> |
   

