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
description: Y-coordenadas do marcador de comentário em coordenadas de páginas.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773317"
---
# <a name="y-cell-annotation-section"></a>Célula Y (Seção Annotation)

*Y* -coordenadas do marcador de comentário em coordenadas de páginas. 
  
> [!NOTE]
> Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd. Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013. 
  
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula Y pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula Y pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice da linha:  <br/> |**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visAnnotationY** <br/> |
   

