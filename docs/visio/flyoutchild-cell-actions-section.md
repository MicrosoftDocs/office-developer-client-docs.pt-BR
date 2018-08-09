---
title: Célula FlyoutChild (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu.
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771899"
---
# <a name="flyoutchild-cell-actions-section"></a>Célula FlyoutChildd (Seção Actions)

Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu. 
  
## <a name="remarks"></a>Comentários

Para obter uma referência à célula FlyoutChild pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações de FlyoutChildwhere.  *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência à célula FlyoutChild pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionFlyoutChild** <br/> |
   

