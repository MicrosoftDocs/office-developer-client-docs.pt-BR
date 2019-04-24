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
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359637"
---
# <a name="lockaspect-cell-protection-section"></a>Célula LockAspect (Seção Protection)

Protege a taxa de proporção da forma para que ela somente seja dimensionada proporcionalmente e não em uma dimensão única.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A taxa de proporção está protegida.  <br/> |
| FALSE  <br/> | A taxa de proporção não está protegida.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LockAspect pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockAspect  <br/> |
   
Para fazer referência à célula LockAspect pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockAspect** <br/> |
   

