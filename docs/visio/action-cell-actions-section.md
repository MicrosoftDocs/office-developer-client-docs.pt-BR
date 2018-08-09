---
title: Célula Action (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771242"
---
# <a name="action-cell-actions-section"></a>Célula Action (Seção Actions)

Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

Uma célula Action é avaliada somente quando ocorre a ação, não quando a fórmula é inserida.
  
Para fazer referência à célula Action pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Ações.  *nome* . Ação onde ações. *nome* é o nome da linha actions  <br/> |
   
Para fazer referência à célula Action pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionAction** <br/> |
| Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visActionAction** <br/> |
   

