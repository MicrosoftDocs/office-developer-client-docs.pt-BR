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
description: Especifica um tipo de dado para o valor do campo de texto.
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773197"
---
# <a name="type-cell-text-fields-section"></a>Célula Type (Seção Text Fields)

Especifica um tipo de dado para o valor do campo de texto.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Sequência de caracteres.  <br/> |
|2  <br/> |Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.  <br/> |
|5  <br/> |Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.  <br/> |
|6  <br/> |Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.  <br/> |
|7  <br/> |Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor desta célula usando a caixa de diálogo **campo** (com a forma selecionada, na guia **Inserir** , no grupo **texto** , clique em **campo** ). 
  
Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Fields.Type [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula Type pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionTextField** <br/> |
|Índice da linha:  <br/> |**visRowField** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visFieldType** <br/> |
   

