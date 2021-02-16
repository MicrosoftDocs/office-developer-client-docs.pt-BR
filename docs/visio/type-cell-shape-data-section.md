---
title: Célula Type (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Especifica um tipo de dados para o valor dados da forma.
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406245"
---
# <a name="type-cell-shape-data-section"></a>Célula Type (Seção Shape Data)

Especifica um tipo de dados para o valor dados da forma.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Sequência de caracteres (padrão).  <br/> |**visPropTypeString** <br/> |
|1   <br/> |Lista fixa. Exibe os itens da lista em uma caixa de combinação suspensa na caixa de diálogo **Definir Dados da Forma**. Especifique os itens da lista na célula Format. Os usuários podem selecionar somente um item da lista.<br/> |**visPropTypeListFix** <br/> |
|2   <br/> |Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeNumber** <br/> |
|3   <br/> |Booliano. Exibe FALSE e TRUE como itens que podem ser selecionados pelo usuário na caixa de lista suspensa da caixa de diálogo **Definir Dados da Forma**.<br/> |**visPropTypeBool** <br/> |
|4   <br/> |Lista variável. Exibe os itens da lista em uma caixa de combinação suspensa na caixa de diálogo **Definir Dados da Forma**. Especifique os itens da lista na célula Format. Os usuários podem selecionar um item da lista ou inserir um novo item adicionado à lista atual na célula Format.<br/> |**visPropTypeListVar** <br/> |
|5   <br/> |Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeDate** <br/> |
|6   <br/> |Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeDuration** <br/> |
|7   <br/> |Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Prop. *Nome*  . Digite onde Prop.  *Nome*  é o nome da linha  <br/> |
   
Para obter uma referência para a célula Type pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionProp** <br/> |
|Índice de linha:  <br/> |**visRowProp**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visCustPropsType** <br/> |
   

