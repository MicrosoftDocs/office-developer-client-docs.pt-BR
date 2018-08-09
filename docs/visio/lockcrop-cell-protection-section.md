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
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772240"
---
# <a name="lockcrop-cell-protection-section"></a>Célula LockCrop (Seção Protection)

Protege um objeto de outro programa de ser recortado com a ferramenta **Cortar**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma não pode ser cortada.  <br/> |
| FALSO  <br/> | A forma pode ser cortada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockCrop pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockCrop  <br/> |
   
Para fazer referência à célula LockCrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockCrop** <br/> |
   

