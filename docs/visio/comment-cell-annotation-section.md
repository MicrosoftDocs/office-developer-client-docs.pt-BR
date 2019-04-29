---
title: Célula Comment (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contém o texto que aparece em um comentário.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415527"
---
# <a name="comment-cell-annotation-section"></a>Célula de Comentários (Seção de Anotação)

Contém o texto que aparece em um comentário.
  
> [!NOTE]
> Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd. Não é usada para rastrear comentários em documentos .vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Comment pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation.Comment[  *i*  ]            onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Comment pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice de linha:  <br/> |**visRowAnnotation ** +  *i*            onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visAnnotationComment** <br/> |
   

