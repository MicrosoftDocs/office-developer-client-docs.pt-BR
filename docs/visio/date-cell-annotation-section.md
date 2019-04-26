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
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360337"
---
# <a name="date-cell-annotation-section"></a>Célula Data (Seção de anotação)

Contém a data e a hora em que o comentário foi editado pela última vez. 
  
> [!NOTE]
> Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd. Não é usada para rastrear comentários em documentos .vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Somente a data é exibida na caixa de comentário na interface do usuário.
  
Para fazer referência à célula Date pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation.Date [  *i*  ]           onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Date pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice de linha:  <br/> |**visRowAnnotation ** +  *i*            onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visAnnotationDate** <br/> |
   

