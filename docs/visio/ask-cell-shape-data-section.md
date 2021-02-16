---
title: Célula Ask (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Determina se um usuário é solicitado a inserir os dados da forma quando uma instância é criada ou a forma é duplicada ou copiada.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426860"
---
# <a name="ask-cell-shape-data-section"></a>Célula Ask (Seção Shape Data)

Determina se um usuário é solicitado a inserir os dados da forma quando uma instância é criada ou a forma é duplicada ou copiada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Solicita ao usuário inserir dados da forma na caixa de diálogo **Definir Dados da Forma**.  <br/> |
|FALSE  <br/> |Não solicita ao usuário inserir dados.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor desta célula corresponde à caixa de seleção **Perguntar ao Soltar** da caixa de diálogo **Definir Dados da Forma** (Clique com o botão direito do mouse na forma, aponte para **Dados** e clique em **Definir Dados da Forma**).
  
Para fazer referência à célula Ask pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Prop. *nome*  . Verifique onde Prop.  *é*  o nome da linha de propriedade personalizada.  <br/> |
   
Para fazer referência à célula Ask pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionProp** <br/> |
|Índice de linha:  <br/> |**visRowProp**  +   *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice de célula:  <br/> |**visCustPropsAsk** <br/> |
   

