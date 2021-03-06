---
title: Célula LockFormat (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Protege a formatação de uma forma impedindo-a de ser alterada.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409675"
---
# <a name="lockformat-cell-protection-section"></a>Célula LockFormat (Seção Protection)

Protege a formatação de uma forma impedindo-a de ser alterada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A formatação não pode ser alterada.  <br/> |
| FALSE  <br/> | A formatação pode ser alterada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockFormat  <br/> |
   
Para fazer referência à célula LockFormat pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockFormat** <br/> |
   

