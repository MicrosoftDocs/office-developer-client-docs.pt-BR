---
title: Célula X (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: A coordenada x do marcador de comentário em coordenadas de página.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434477"
---
# <a name="x-cell-annotation-section"></a>Célula X (Seção Annotation)

A  *coordenada x*  do marcador de comentário em coordenadas de página. 
  
> [!NOTE]
> Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd. Não é usada para rastrear comentários em documentos .vsdx no Visio 2013. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Annotation.X[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAnnotation** <br/> |
| Índice de linha:  <br/> |**visRowAnnotation** +  *i*            onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visAnnotationX** <br/> |
   

