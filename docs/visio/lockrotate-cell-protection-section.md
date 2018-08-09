---
title: Célula LockRotate (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Trava as formas 2D para impedir que sejam giradas com a alça de rotação ou com o comando Girar 90° para a esquerda ou Girar 90° para a direita.
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772261"
---
# <a name="lockrotate-cell-protection-section"></a>Célula LockRotate (Seção Protection)

Trava as formas 2D para impedir que sejam giradas com a alça de rotação ou com o comando **Girar 90° para a esquerda** ou **Girar 90° para a direita**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma não pode ser girada.  <br/> |
| FALSO  <br/> | A forma pode ser girada (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

A célula LockRotate não impedirá uma forma 1D de ser girada quando um ponto de extremidade for arrastado. Para proteger uma forma 1D contra a rotação, defina a célula LockWidth como um valor diferente de zero (VERDADEIRO).
  
Para fazer referência à célula LockRotate pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LockRotate  <br/> |
   
Para fazer referência à célula LockRotate pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLock** <br/> |
| Índice da célula:  <br/> |**visLockRotate** <br/> |
   

