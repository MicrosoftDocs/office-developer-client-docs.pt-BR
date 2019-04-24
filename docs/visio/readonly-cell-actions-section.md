---
title: Célula ReadOnly (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Controla se a ação em um menu de marca de ação ou atalho é somente leitura ou não.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359987"
---
# <a name="readonly-cell-actions-section"></a>Célula ReadOnly (Seção Actions)

Controla se a ação em um menu de atalho ou de marca de ação é somente leitura. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |A ação é exibida no menu, mas é somente leitura.  <br/> |
|FALSE  <br/> |A ação é exibida no menu e pode ser selecionada (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Quando uma ação é somente leitura, ela é exibida no menu de atalho ou de marca de ação, mas você não pode selecioná-la. Ela não fica esmaecida, é exibida em fundo colorido, como um rótulo. Para que o item de menu seja exibido esmaecido, use a célula Disabled. 
  
Para obter uma referência para a célula ReadOnly pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações Readonlyonde.  *Name* é o nome da linha de ações  <br/> |
   
Para obter uma referência para a célula ReadOnly pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionReadOnly** <br/> |
   

