---
title: Célula QuickStyleVariation (seção de estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina se devem ser substituídas as fórmulas e os valores de texto, linha e preenchimento cor (ou uma combinação dessas propriedades) usando cores que contraste com o plano de fundo do diagrama. O valor é um OR bit a bit 0, 1, 2, 4 e 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772632"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>Célula QuickStyleVariation (seção de estilos rápidos)

Determina se devem ser substituídas as fórmulas e os valores de texto, linha e preenchimento cor (ou uma combinação dessas propriedades) usando cores que contraste com o plano de fundo do diagrama. O valor é um OR bit a bit 0, 1, 2, 4 e 8.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Não altere o texto de uma forma, linha, ou preenchimento cor (ou qualquer combinação dessas propriedades) para permanecer visível contra a cor de plano de fundo determinado de um tema.  <br/> |
|1  <br/> |Não altere o texto de uma forma, linha, ou preenchimento cor (ou qualquer combinação dessas propriedades) para permanecer visível contra a cor de plano de fundo determinado de um tema.  <br/> |
|2  <br/> |Altere a cor do texto de uma forma, se necessário, permaneça visível contra um tema determinados cor de plano de fundo.  <br/> |
|4  <br/> |Altere a cor da linha de uma forma, se necessário, permaneça visível contra um tema determinados cor de plano de fundo.  <br/> |
|8  <br/> |Altere a cor de preenchimento de uma forma, se necessário, permaneça visível contra um tema determinados cor de plano de fundo.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Use a célula QuickStyleVariation para garantir a visibilidade em texto ou linhas quando estiverem fora qualquer geometria da forma visível (por exemplo, em uma forma cujo textbox é abaixo da parte inferior da forma, como aquelas nos diagramas de rede). O valor da célula padrão é 0, o que significa que seu comportamento está inativo. Qualquer outro valor dispara o comportamento da célula.
  
O valor de QuickStyleVariation substitui o valor produzido pela função THEMEVAL quando ele reside na cor (seção Character), FillForegnd ou LineColor células (ou geradas pelo referências diretas para essas três propriedades por meio de THEMEVAL (" CharacterColor"), THEMEVAL("FillColor") e THEMEVAL("LineColor")).
  
Para obter uma referência à célula **QuickStyleVariation** pelo nome, a partir de outra fórmula, fazendo com que o valor do atributo **N** de um elemento de **célula** ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |QuickStyleVariation  <br/> |
   
Para obter uma referência à célula **QuickStyleVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowQuickStyleProperties** <br/> |
|Índice da célula:  <br/> |**visQuickStyleVariation** <br/> |
   

