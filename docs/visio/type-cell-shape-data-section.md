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
description: Especifica um tipo de dado para o valor de dados da forma.
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773196"
---
# <a name="type-cell-shape-data-section"></a>Célula Type (Seção Shape Data)

Especifica um tipo de dado para o valor de dados da forma.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Sequência de caracteres (padrão).  <br/> |**visPropTypeString** <br/> |
|1  <br/> |Lista fixa. Exibe os itens de lista em uma combinação suspensa caixa na caixa de diálogo **Definir dados da forma** . Especifique os itens da lista na célula Format. Os usuários podem selecionar somente um item da lista.  <br/> |**visPropTypeListFix** <br/> |
|2  <br/> |Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Boolean. Exibe Falso e verdadeiro como itens que os usuários podem selecionar de uma caixa de listagem suspensa na caixa de diálogo **Definir dados da forma** .  <br/> |**visPropTypeBool** <br/> |
|4  <br/> |Lista variável. Exibe os itens de lista em uma combinação suspensa caixa na caixa de diálogo **Definir dados da forma** . Especifique os itens da lista na célula Format. Os usuários podem selecionar um item de lista ou digitar um novo item é adicionado à lista atual na célula Format.  <br/> |**visPropTypeListVar** <br/> |
|5  <br/> |Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeDate** <br/> |
|6  <br/> |Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Prop. *Nome* . Tipo onde Prop.  *Name* é o nome da linha  <br/> |
   
Para obter uma referência à célula Type pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionProp** <br/> |
|Índice da linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCustPropsType** <br/> |
   

