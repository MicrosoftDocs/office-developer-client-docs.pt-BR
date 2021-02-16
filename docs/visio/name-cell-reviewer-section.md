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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417683"
---
# <a name="name-cell-reviewer-section"></a>Célula Name (Seção Reviewer)

Contém o nome do revisor de um documento.
  
## <a name="remarks"></a>Comentários

 Esse valor assume como padrão  o nome encontrado  na caixa Nome de usuário, na  guia Geral da caixa de diálogo Opções do **Visio** (clique na guia Arquivo, em Opções e em **Geral).** 
  
Para fazer referência à célula Name pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Reviewer.Name [  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula Name pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionReviewer** <br/> |
| Índice de linha:  <br/> |**visRowReviewer**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visReviewerName** <br/> |
   

