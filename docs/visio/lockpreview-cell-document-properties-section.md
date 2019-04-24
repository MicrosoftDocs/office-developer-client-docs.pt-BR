---
title: Célula LockPreview (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Determina se uma visualização será salva sempre que um desenho for salvo.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348325"
---
# <a name="lockpreview-cell-document-properties-section"></a>Célula LockPreview (Seção Document Properties)

Determina se uma visualização será salva sempre que um desenho for salvo.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | Não salvar uma visualização sempre que um desenho for salvo.  <br/> |
| FALSE  <br/> | Salvar uma visualização sempre que um desenho for salvo.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockPreview pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockPreview  <br/> |
   
Para fazer referência à célula LockPreview pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocLockPreview** <br/> |
   

