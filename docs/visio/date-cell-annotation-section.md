---
title: Célula Date (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contém a data e a hora em que o comentário foi editado pela última vez.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771673"
---
# <a name="date-cell-annotation-section"></a>Célula Date (Seção Annotation)

Contém a data e a hora em que o comentário foi editado pela última vez. 
  
> [!NOTE]
> Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd. Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Somente a data é exibida na caixa de comentário na interface do usuário.
  
Para fazer referência à célula Date pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation.Date [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Date pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice da linha:  <br/> |**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visAnnotationDate** <br/> |
   

