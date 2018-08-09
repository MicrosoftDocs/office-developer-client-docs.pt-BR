---
title: Célula LockGroup (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Protege um grupo impedindo-o de ser desagrupado.
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772265"
---
# <a name="lockgroup-cell-protection-section"></a>Célula LockGroup (Seção Protection)

Protege um grupo impedindo-o de ser desagrupado.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O grupo não pode ser desagrupado.  <br/> |
|FALSO  <br/> |O grupo pode ser desagrupado.  <br/> |
   
## <a name="remarks"></a>Comentários

A definição do valor LockGroupCell como TRUE também impede a exclusão de formas que sejam membros do grupo.
  
Para obter uma referência para a célula LockGroup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LockGroup  <br/> |
   
Para obter uma referência para a célula LockGroup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLock** <br/> |
|Índice da célula:  <br/> |**visLockGroup** <br/> |
   

