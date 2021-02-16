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
description: Resulta em uma cadeia de caracteres que influencia a ordem na qual os itens na janela Dados da Forma são listados.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417851"
---
# <a name="sortkey-cell-shape-data-section"></a>Célula SortKey (Seção Shape Data)

Avalia uma cadeia de caracteres que influencia a ordem em que os itens são listados na janela **Dados de Forma**. 
  
## <a name="remarks"></a>Comentários

O cálculo utilizado para comparar os valores da célula SortKey são específicos à localidade e sem diferenciação de maiúsculas e minúsculas. Se os valores de SortKey forem iguais, os dados da forma serão listados em fila. Os dados da forma que não têm chave de classificação são listados após os dados da forma que contêm uma chave de classificação.
  
O exemplo a seguir mostra como utilizar as chaves de classificação para exibir os dados de forma na janela **Dados da Forma** na ordem: Número de Itens, Quantidade, Preço. 
  
 *Row, Label e*  *SortKey*  referem-se às células na linha de dados da forma. Neste caso, as linhas de dados de forma foram nomeadas. 
  
|**Linha**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Número de itens  <br/> | 1   <br/> |
| Prop.Price  <br/> | Price  <br/> | 3   <br/> |
| Prop.Quan  <br/> | Quantidade  <br/> | 2   <br/> |
   
Para obter uma referência para a célula SortKey pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *Nome*  . SortKey onde Prop.  *Nome*  é o nome da linha de propriedade personalizada  <br/> |
   
Para obter uma referência para a célula SortKey pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice de linha:  <br/> |**visRowProp**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCustPropsSortKey** <br/> |
   

