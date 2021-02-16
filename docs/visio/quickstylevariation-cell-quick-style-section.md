---
title: Célula QuickStyleVariation (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina se deve substituir as fórmulas e os valores de texto, linha e cor de preenchimento (ou uma combinação dessas propriedades) usando cores que contrastam com o plano de fundo do diagrama. O valor é um BIT OR de 0, 1, 2, 4 e 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433791"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>Célula QuickStyleVariation (Seção Quick Style)

Determina se deve substituir as fórmulas e os valores de texto, linha e cor de preenchimento (ou uma combinação dessas propriedades) usando cores que contrastam com o plano de fundo do diagrama. O valor é um BIT OR de 0, 1, 2, 4 e 8.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Não altere a cor de preenchimento, linha ou texto de uma forma (ou qualquer combinação dessas propriedades) para permanecer visível em relação à cor de plano de fundo determinada de um tema.  <br/> |
|1   <br/> |Não altere a cor de preenchimento, linha ou texto de uma forma (ou qualquer combinação dessas propriedades) para permanecer visível em relação à cor de plano de fundo determinada de um tema.  <br/> |
|2   <br/> |Altere a cor do texto de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.  <br/> |
|4   <br/> |Altere a cor da linha de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.  <br/> |
|8   <br/> |Altere a cor de preenchimento de uma forma, se necessário, para permanecer visível em relação à cor de plano de fundo determinada de um tema.  <br/> |
   
## <a name="remarks"></a>Comentários

Use a célula QuickStyleVariation para garantir a visibilidade em texto ou linhas quando elas estão fora de qualquer geometria de forma visível (por exemplo, em uma forma cuja caixa de texto está abaixo da parte inferior da forma, como aquelas em Diagramas de Rede). O valor padrão da célula é 0, o que significa que seu comportamento está inativo. Qualquer outro valor aciona o comportamento da célula.
  
O valor QuickStyleVariation substitui o valor produzido pela função THEMEVAL quando reside nas células Color (Seção Character), FillForegnd ou LineColor (ou produzido por referências diretas a essas três propriedades por meio de THEMEVAL("CharacterColor"), THEMEVAL("FillColor") e THEMEVAL("LineColor")).
  
Para obter uma referência para a célula **QuickStyleVariation** pelo nome, a partir de outra fórmula, ao obter o valor do atributo **N** de um elemento **Cell** ou de um programa usando a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |QuickStyleVariation  <br/> |
   
Para fazer referência à **célula QuickStyleVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowQuickStyleProperties** <br/> |
|Índice de célula:  <br/> |**visQuickStyleVariation** <br/> |
   

