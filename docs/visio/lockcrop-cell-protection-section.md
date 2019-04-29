---
title: Célula LockCrop (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Protege um objeto de outro programa de ser recortado com a ferramenta Cortar.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411852"
---
# <a name="lockcrop-cell-protection-section"></a>Célula LockCrop (Seção Protection)

Protege um objeto de outro programa de ser recortado com a ferramenta **Cortar**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma não pode ser cortada.  <br/> |
| FALSE  <br/> | A forma pode ser cortada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockCrop pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockCrop  <br/> |
   
Para fazer referência à célula LockCrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockCrop** <br/> |
   

