---
title: Célula Type (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Especifica um tipo de dados para o campo de texto.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407981"
---
# <a name="type-cell-text-fields-section"></a>Célula Type (Seção Text Fields)

Especifica um tipo de dados para o campo de texto.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Cadeia de caracteres.  <br/> |
|duas  <br/> |Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.  <br/> |
|5   <br/> |Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.  <br/> |
|6   <br/> |Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.  <br/> |
|7   <br/> |Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula usando a caixa de diálogo **campo** (com uma forma selecionada, na guia **Inserir** , no grupo **texto** , clique em **campo** ). 
  
Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Fields. Type [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Type pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionTextField** <br/> |
|Índice de linha:  <br/> |**visRowField** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visFieldType** <br/> |
   

