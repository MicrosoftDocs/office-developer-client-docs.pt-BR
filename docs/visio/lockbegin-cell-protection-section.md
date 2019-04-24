---
title: Célula LockBegin (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Protege o ponto inicial (BeginX, BeginY) de uma forma 1D para uma localização específica.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359644"
---
# <a name="lockbegin-cell-protection-section"></a>Célula LockBegin (Seção Protection)

Protege o ponto inicial (BeginX, BeginY) de uma forma 1D para uma localização específica.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | O ponto inicial está protegido.  <br/> |
| FALSE  <br/> | O ponto inicial não está protegido.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockBegin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockBegin  <br/> |
   
Para fazer referência à célula LockBegin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockBegin** <br/> |
   

