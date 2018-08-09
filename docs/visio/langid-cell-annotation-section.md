---
title: Célula LangID (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indica o idioma no qual o comentário foi inserido.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772147"
---
# <a name="langid-cell-annotation-section"></a>Célula LangID (Seção Annotation)

Indica o idioma no qual o comentário foi inserido.
  
> [!NOTE]
> Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd. Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Esse valor é a identificação de localidade (LCID) do idioma ativo na barra de idioma quando o comentário foi inserido. Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office oferecem suporte, consulte o tópico da célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties). 
  
Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation.LangID [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice da linha:  <br/> |**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visAnnotationLangID** <br/> |
   

