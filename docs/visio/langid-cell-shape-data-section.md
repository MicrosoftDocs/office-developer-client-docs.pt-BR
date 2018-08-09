---
title: Célula LangID (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indica o idioma no qual o valor dos dados da forma foi inserido.
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772166"
---
# <a name="langid-cell-shape-data-section"></a>Célula LangID (Seção Shape Data)

Indica o idioma no qual o valor dos dados da forma foi inserido. 
  
## <a name="remarks"></a>Comentários

Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office System oferecem suporte, consulte a célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties). 
  
Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *nome* . LangID onde Prop.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice da linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsLangID** <br/> |
   

