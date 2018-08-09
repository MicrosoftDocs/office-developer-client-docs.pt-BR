---
title: Célula Menu (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Define o nome de um item de menu exibido em um menu de atalho ou de marca de ação para uma forma ou página.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772418"
---
# <a name="menu-cell-actions-section"></a>Célula Menu (Seção Actions)

Define o nome de um item de menu exibido em um menu de atalho ou de marca de ação para uma forma ou página. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

Para inserir um separador no menu acima desse item, use a célula BeginGroup. Para exibir o comando na parte inferior do menu, insira antes do nome o caractere de porcentagem (%) .
  
Para obter uma referência para a célula Menu pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações de Menuwhere.  *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula Menu pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde i = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visActionMenu** <br/> |
   

