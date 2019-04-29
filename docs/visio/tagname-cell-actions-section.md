---
title: Célula TagName (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contém o nome da marca de ação a que esta ação está associada.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412713"
---
# <a name="tagname-cell-actions-section"></a>Célula TagName (Seção Actions)

Contém o nome da marca de ação a que esta ação está associada.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

A célula TagName na seção Actions trabalha junto com a célula TagName na seção Action Tags para associar a marca de ação a suas ações. 
  
- Se a célula TagName em uma linha Actions estiver em branco, a ação será exibida em um menu de atalho, não em um menu de marca de ação.
    
- Se um valor de célula TagName na linha Actions corresponder ao valor da célula TagName em uma linha Smart Tags, a ação será exibida no menu de marca de ação.
    
- Se a célula TagName de uma ação tiver um valor, mas não corresponder ao valor TagName em qualquer linha de marca de forma, essa ação não aparecerá nos menus de marcas de ação ou nos menus de atalho.
    
- Se várias linhas da marca inteligente tiverem o mesmo valor TagName, todas exibirão as mesmas ações.
    
Para obter uma referência para a célula TagName pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações Tagnameonde.  *Name* é o nome da linha de ações  <br/> |
   
Para fazer referência à célula TagName pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice de linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionTagName** <br/> |
   

