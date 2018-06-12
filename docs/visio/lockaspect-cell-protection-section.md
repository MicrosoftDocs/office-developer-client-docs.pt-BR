---
title: Célula LockAspect (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Protege a taxa de proporção da forma para que ela somente seja dimensionada proporcionalmente e não em uma dimensão única.
ms.openlocfilehash: fb5736add65f548f06697077bc539ec7fac5feb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772239"
---
# <a name="lockaspect-cell-protection-section"></a>Célula LockAspect (Seção Protection)

Protege a taxa de proporção da forma para que ela somente seja dimensionada proporcionalmente e não em uma dimensão única.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A taxa de proporção está protegida.  <br/> |
| FALSO  <br/> | A taxa de proporção não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula LockAspect pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockAspect  <br/> |
   
Para obter uma referência à célula LockAspect pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockAspect** <br/> |
   

