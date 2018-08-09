---
title: Célula BeginGroup (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indica se um separador está inserido no menu acima desta ação.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771294"
---
# <a name="begingroup-cell-actions-section"></a>Célula BeginGroup (Seção Actions)

Indica se um separador está inserido no menu acima desta ação. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |
          Um separador está inserido no menu acima desta ação. 
  <br/> |
|FALSO  <br/> |
          Um separador não está inserido no menu acima desta ação.
  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula BeginGroup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome*. BeginGroup onde ações. *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula BeginGroup pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionBeginGroup** <br/> |
   

