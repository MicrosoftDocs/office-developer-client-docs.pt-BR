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
description: Indica se um separador deve ser inserido no menu acima desta ação.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407834"
---
# <a name="begingroup-cell-actions-section"></a>Célula BeginGroup (Seção Ações)

Indica se um separador deve ser inserido no menu acima desta ação. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Um separador deve ser inserido no menu acima desta ação.  <br/> |
|FALSO  <br/> |Um separador não está inserido no menu acima desta ação.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula BeginGroup por nome de outra fórmula ou de um programa que utiliza a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome*.BeginGroup onde Ações. *nome* é o nome da linha Ações  <br/> |
   
Para obter uma referência à célula BeginGroup por índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice de linha:  <br/> |**visRowAction** +  *i*           onde  *i*  = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visActionBeginGroup** <br/> |
   

