---
title: Célula Format (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
localization_priority: Normal
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Especifica a formatação de um item de dados da forma que pode ser uma sequência de caracteres, uma lista fixa, um número, uma lista variável, uma data ou hora, uma duração ou uma moeda.
ms.openlocfilehash: bb02cfefd6dc93798ca5e2b0c657e4616515fd0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415359"
---
# <a name="format-cell-shape-data-section"></a>Célula Format (Seção Shape Data)

Especifica a formatação de um item de dados da forma que pode ser uma sequência de caracteres, uma lista fixa, um número, uma lista variável, uma data ou hora, uma duração ou uma moeda.
  
## <a name="remarks"></a>Comentários

|**Tipo de item de dados da forma**|**Valor**|**Conteúdo da célula Format**|
|:-----|:-----|:-----|
| String  <br/> | ,0  <br/> | Uma figura de formatação apropriada para o tipo de dado.  <br/> |
| Lista fixa  <br/> | 1  <br/> | Os itens a serem exibidos na lista, separados por ponto-e-vírgula.  <br/> |
| Número  <br/> | duas  <br/> | Uma figura de formatação apropriada para o tipo de dado.  <br/> |
| Lista variável  <br/> | 4   <br/> | Os itens a serem exibidos na lista, separados por ponto-e-vírgula.  <br/> |
| Data ou hora  <br/> | 5   <br/> | Uma figura de formatação apropriada para o tipo de dado.  <br/> |
| Duração  <br/> | 6   <br/> | Uma figura de formatação apropriada para o tipo de dado.  <br/> |
| Moeda  <br/> | 7   <br/> | Uma figura de formatação apropriada para o tipo de dado.  <br/> |
   
Um exemplo de especificação de uma figura de formatação apropriada para o tipo de dado é a figura de formatação "# #/4 UU" que formata o número 12,43 pol. como 12 2/4 POLEGADAS. Para obter mais informações sobre como especificar uma figura de formatação, consulte [Sobre figuras de formatação](about-format-pictures.md).
  
Um exemplo de itens de especificação de uma lista é "Engenharia;Recursos humanos;Vendas;Marketing".
  
Os valores de data (tipo = 5) são exibidos no formato de data abreviada. Os valores de moeda (tipo = 7) são exibidos usando a configuração atual do usuário para **Moeda** na guia **Opções Regionais** no item **Opções Regionais e de Idioma** do **Painel de Controle**.
  
Um número (tipo = 2) pode representar uma dimensão, uma grandeza escalar, um ângulo, uma data, uma hora ou uma moeda. Para garantir que um número de entrada seja sempre avaliado como uma data, hora ou moeda, utilize as funções DATETIME ou CY na célula Format em vez de uma figura de formatação.
  
Para fazer referência à célula Format pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hélice.  *nome* . Formatar onde prop.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula Format pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice de linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsFormat** <br/> |
   

