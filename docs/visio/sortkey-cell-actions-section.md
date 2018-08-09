---
title: Célula SortKey (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Um número que determina a ordem de ações exibidas em um menu de atalho ou de marca de ação.
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773054"
---
# <a name="sortkey-cell-actions-section"></a>Célula SortKey (Seção Actions)

Um número que determina a ordem de ações exibidas em um menu de atalho ou de marca de ação.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

As ações em um menu de atalho ou de marca de ação são exibidas no menu, classificadas do valor mais baixo para o mais alto, com a numeração mais baixa exibida na parte superior do menu. Se duas linhas de ação tiverem o mesmo valor de célula SortKey, a ordem será determinada pela ordem física da linha. O padrão é 0 (zero).
  
Para obter uma referência para a célula SortKey pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações de SortKeywhere.  *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula SortKey pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionSortKey** <br/> |
   

