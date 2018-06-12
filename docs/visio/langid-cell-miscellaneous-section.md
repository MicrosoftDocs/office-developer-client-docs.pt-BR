---
title: Célula LangID (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Indica o idioma no qual as fórmulas das células foram criadas.
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772186"
---
# <a name="langid-cell-miscellaneous-section"></a>Célula LangID (Seção Miscellaneous)

Indica o idioma no qual as fórmulas das células foram criadas. 
  
## <a name="remarks"></a>Comentários

Para obter uma lista de idiomas suportados pelos aplicativos do Microsoft Office, consulte o tópico do [DocLangID](doclangid-cell-document-properties-section.md) (seção Document Properties) da célula. 
  
Para obter uma referência à célula LangID pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LangID  <br/> |
   
Para obter uma referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visObjLangID** <br/> |
   

