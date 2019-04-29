---
title: Célula ComplexScriptSize (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428435"
---
# <a name="complexscriptsize-cell-character-section"></a>Célula ComplexScriptSize (Seção Caracteres)

O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos. 
  
## <a name="remarks"></a>Comentários

Tamanhos de fonte de script complexos são listados na guia **Fonte** na caixa de diálogo **Texto** (clique na seta no grupo **Fonte** na guia **Início**). Essa lista só é exibida se você tiver adicionado um idioma que contenha caracteres Asiáticos ou de script complexo, na caixa de diálogo **Preferências de Idioma do Microsoft Office**. (Clique em **Iniciar**, em **Todos os programas**, em **Microsoft Office**, em **Ferramentas do Microsoft Office** e em **Preferências de Idioma do Microsoft Office**.
  
Você pode inserir esse valor como um tamanho de ponto explícito ou como um percentual. Se você especificar um percentual, o valor é baseado no valor da célula Size. O valor padrão 0 (zero) significa 100%. 
  
Para obter uma referência à célula ComplexScriptSize pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.ComplexScriptSize[ *i*  ]           onde  *i*  = <1>, 2, 3...  <br/> |
   
Para obter uma referência à célula ComplexScriptSize pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice de linha:  <br/> |**visRowCharacter** +  *i*           onde  *i*  = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

