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
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422254"
---
# <a name="langid-cell-annotation-section"></a>Célula LangID (Seção Annotation)

Indica o idioma no qual o comentário foi inserido.
  
> [!NOTE]
> Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd. Não é usada para rastrear comentários em documentos .vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Esse valor é a identificação de localidade (LCID) do idioma ativo na barra de idioma quando o comentário foi inserido. Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office oferecem suporte, consulte o tópico da célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties). 
  
Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation. LangID [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice de linha:  <br/> |**visRowAnnotation ** +  *i*            onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visAnnotationLangID** <br/> |
   

