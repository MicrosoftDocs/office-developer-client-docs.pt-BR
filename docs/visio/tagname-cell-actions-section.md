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
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773111"
---
# <a name="tagname-cell-actions-section"></a>Célula TagName (Seção Actions)

Contém o nome da marca de ação a que esta ação está associada.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

A célula TagName na seção Actions trabalha junto com a célula TagName na seção Action Tags para associar a marca de ação a suas ações. 
  
- Se a célula TagName em uma linha Actions estiver em branco, a ação é exibida em um menu de atalho, não em um menu de marca de ação.
    
- Se o valor da célula TagName na linha Actions corresponder ao valor da célula TagName em uma linha Smart Tags, a ação é exibida no menu de marca de ação.
    
- Se a célula TagName de uma ação tem um valor, mas não corresponde ao valor TagName em qualquer linha da marca de forma, essa ação não aparecem nos qualquer menus de marca de ação ou os menus de atalho.
    
- Se várias linhas da marca inteligente tiverem o mesmo valor TagName, todas exibirão as mesmas ações.
    
Para obter uma referência à célula TagName pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações de TagNamewhere.  *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência à célula TagName pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionTagName** <br/> |
   

