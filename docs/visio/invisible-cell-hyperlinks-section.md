---
title: Célula Invisible (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indica se um hiperlink será exibido no menu de atalho para uma forma ou página.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772094"
---
# <a name="invisible-cell-hyperlinks-section"></a>Célula Invisible (Seção Hyperlinks)

Indica se um hiperlink será exibido no menu de atalho para uma forma ou página. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O hiperlink não é exibido como um item de menu no menu de atalho.  <br/> |
|FALSO  <br/> |O hiperlink é exibido como um item de menu no menu de atalho (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula Invisible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *nome* . Invisível onde Hyperlink *. nome* é o nome da linha  <br/> |
   
Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
|Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visHLinkInvisible** <br/> |
   

