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
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404628"
---
# <a name="invisible-cell-hyperlinks-section"></a>Célula Invisible (Seção Hyperlinks)

Indica se um hiperlink será exibido no menu de atalho para uma forma ou página. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O hiperlink não é exibido como um item de menu no menu de atalho.  <br/> |
|FALSE  <br/> |O hiperlink é exibido como um item de menu no menu de atalho (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula Invisible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *nome*  . Invisível onde Hyperlink  *.name é*  o nome da linha  <br/> |
   
Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
|Índice de linha:  <br/> |**visRow1stHyperlink**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visHLinkInvisible** <br/> |
   

