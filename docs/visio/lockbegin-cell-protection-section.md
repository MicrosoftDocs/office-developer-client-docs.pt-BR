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
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772228"
---
# <a name="lockbegin-cell-protection-section"></a>Célula LockBegin (Seção Protection)

Protege o ponto inicial (BeginX, BeginY) de uma forma 1D para uma localização específica.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O ponto inicial está protegido.  <br/> |
| FALSO  <br/> | O ponto inicial não está protegido.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula LockBegin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockBegin  <br/> |
   
Para obter uma referência à célula LockBegin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockBegin** <br/> |
   

