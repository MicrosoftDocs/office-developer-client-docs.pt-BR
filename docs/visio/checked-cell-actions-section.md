---
title: Célula Checked (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Indica se um item é verificado no menu de atalho ou marca de ação.
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771517"
---
# <a name="checked-cell-actions-section"></a>Célula Checked (Seção Actions)

Indica se um item é verificado no menu de atalho ou marca de ação.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |
          A marca de seleção é exibida.
  <br/> |
|FALSO  <br/> |
          A marca de seleção não é exibida (padrão).
  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula Checked pelo nome, de outra fórmula ou de um programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Verificado onde ações. *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula Checked pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visActionChecked** <br/> |
   

