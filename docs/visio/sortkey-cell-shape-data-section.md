---
title: Célula SortKey (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Avalia uma cadeia de caracteres que influencia a ordem na qual os itens na janela dados da forma são listados.
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773043"
---
# <a name="sortkey-cell-shape-data-section"></a>Célula SortKey (Seção Shape Data)

Avalia uma cadeia de caracteres que influencia a ordem na qual os itens na janela **Dados** da forma são listados. 
  
## <a name="remarks"></a>Coment�rios

O cálculo usado para comparar valores de SortKey é específica de localidade e maiusculas de minúsculas. Se os valores de SortKey forem iguais, os dados da forma estão listados na ordem de linha. Dados da forma que possuem sem chave de classificação são listados depois que os dados de forma que contêm uma chave de classificação.
  
A seguir está um exemplo de como usar chaves de classificação para exibir os dados da forma na janela **Dados da forma** na ordem: número de itens, quantidade, preço. 
  
 *Row, Label* e *SortKey* se referir a células na linha de dados de forma. Nesse caso, as linhas de dados de forma tenham sido chamadas. 
  
|**Row**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Número de itens  <br/> | 1  <br/> |
| Prop  <br/> | Preço  <br/> | 3  <br/> |
| Prop.Quan  <br/> | Quantidade  <br/> | 2  <br/> |
   
Para obter uma referência para a célula SortKey pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *Nome* . SortKey onde Prop.  *Nome* é o nome da linha de propriedade personalizada  <br/> |
   
Para obter uma referência para a célula SortKey pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice da linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsSortKey** <br/> |
   

