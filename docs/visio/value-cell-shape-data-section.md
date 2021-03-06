---
title: Célula Value (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contém o valor do item de dados de forma conforme inserido na caixa de diálogo Dados da Forma.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431901"
---
# <a name="value-cell-shape-data-section"></a>Célula Value (Seção Shape Data)

Contém o valor do item de dados da forma inserido na caixa de diálogo **Definir Dados da Forma**. 
  
## <a name="remarks"></a>Comentários

As fórmulas inseridas nesta célula são substituídas por valores inseridos na caixa de diálogo **Definir Dados da Forma**. Isso acontecerá mesmo se você utilizar a função GUARD para proteger a fórmula. 
  
Para obter uma referência para a célula Value pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *Nome*  . Valor onde Prop.  *Nome*  é o nome da linha  <br/> |
   
Para fazer referência à célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice de linha:  <br/> |**visRowProp**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCustPropsValue** <br/> |
   

