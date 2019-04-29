---
title: Célula Invisible (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Especifica se o item de dados de forma ficará visível na janela Dados da Forma.
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405314"
---
# <a name="invisible-cell-shape-data-section"></a>Célula Invisible (Seção Shape Data)

Especifica se o item de dados da forma será visível na janela **Dados da Forma**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O item de dados da forma não é visível.  <br/> |
| FALSE  <br/> | O item de dados da forma é visível.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor desta célula corresponde à caixa de seleção **Oculto** da caixa de diálogo **Definir Dados da Forma** (Clique com o botão direito do mouse na forma, aponte para **Dados** e clique em **Definir Dados da Forma**).
  
Para obter uma referência para a célula Invisible pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hélice.  *nome* . Invisível onde prop.  *Name* é o nome da linha  <br/> |
   
Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice de linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsInvis** <br/> |
   

