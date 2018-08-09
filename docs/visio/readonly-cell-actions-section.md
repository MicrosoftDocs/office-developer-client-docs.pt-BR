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
description: Controla se a ação em um menu de atalho ou de marca de ação é somente leitura.
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772637"
---
# <a name="readonly-cell-actions-section"></a>Célula ReadOnly (Seção Actions)

Controla se a ação em um menu de atalho ou de marca de ação é somente leitura. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A ação é exibida no menu, mas é somente leitura.  <br/> |
|FALSO  <br/> |A ação é exibida no menu e pode ser selecionada (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Quando uma ação é somente leitura, ela será exibida no menu de atalho ou de marca de ação, mas você não pode selecioná-la. Ele não estiver esmaecido, mas, é exibida em um plano de fundo colorido, como um rótulo. Para fazer com que o item de menu aparece esmaecido, use a célula Disabled. 
  
Para obter uma referência para a célula ReadOnly pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações de ReadOnlywhere.  *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula ReadOnly pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionReadOnly** <br/> |
   

