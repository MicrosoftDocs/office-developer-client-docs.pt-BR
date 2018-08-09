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
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771554"
---
# <a name="complexscriptsize-cell-character-section"></a>Célula ComplexScriptSize (Seção Character)

O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos. 
  
## <a name="remarks"></a>Comentários

Tamanhos de fonte de script complexo são listados na guia **fonte** da caixa de diálogo **texto** (clique na seta na **fonte** de grupo na guia **página inicial** ). Esta lista é exibida somente se você tiver adicionado um idioma que contém caracteres asiáticos ou de script complexo, na caixa de diálogo **Preferências de idioma do Microsoft Office** . (Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.
  
Você pode inserir esse valor como um tamanho de ponto explícito ou como um percentual. Se você especificar um percentual, o valor é baseado no valor da célula Size. O valor padrão 0 (zero) significa 100%. 
  
Para obter uma referência para a célula ComplexScriptFont pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.ComplexScriptSize [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula ComplexScriptSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

