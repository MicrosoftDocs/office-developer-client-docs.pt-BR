---
title: Célula LockEnd (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Protege o ponto de extremidade (EndX, EndY) de uma forma 1D para uma localização específica.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425579"
---
# <a name="lockend-cell-protection-section"></a>Célula LockEnd (Seção Protection)

Protege o ponto de extremidade (EndX, EndY) de uma forma 1D para uma localização específica.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O ponto de extremidade está protegido.  <br/> |
| FALSE  <br/> | O ponto de extremidade não está protegido.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockEnd pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockEnd  <br/> |
   
Para fazer referência à célula LockEnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockEnd** <br/> |
   

