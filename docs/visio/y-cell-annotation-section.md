---
title: Célula Y (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: A coordenada y do marcador de comentário em coordenadas de páginas.
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360120"
---
# <a name="y-cell-annotation-section"></a>Célula Y (Seção Annotation)

A coordenada *y* do marcador de comentário em coordenadas de páginas. 
  
> [!NOTE]
> Esta célula é usada para rastrear comentários somente ao abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd. Ele não é usado para controlar comentários em documentos. vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation. Y [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice da linha:  <br/> |**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visAnnotationY** <br/> |
   

