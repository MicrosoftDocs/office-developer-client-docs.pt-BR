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
description: Contém o texto exibido em um comentário.
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771520"
---
# <a name="comment-cell-annotation-section"></a>Célula Comment (Seção Annotation)

Contém o texto exibido em um comentário.
  
> [!NOTE]
> Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd. Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Comment pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation.Comment [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Comment pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice da linha:  <br/> |**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visAnnotationComment** <br/> |
   

