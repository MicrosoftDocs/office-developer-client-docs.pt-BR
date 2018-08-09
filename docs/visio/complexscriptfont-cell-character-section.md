---
title: Célula ComplexScriptFont (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contém o número da fonte utilizada para formatar o texto composto de caracteres de script complexos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771549"
---
# <a name="complexscriptfont-cell-character-section"></a>Célula ComplexScriptFont (Seção Character)

Contém o número da fonte utilizada para formatar o texto composto de caracteres de script complexos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. 
  
## <a name="remarks"></a>Comentários

Tamanhos de fonte de script complexo são listados na guia **fonte** da caixa de diálogo **texto** (clique na seta na **fonte** de grupo na guia **página inicial** ). Esta lista é exibida somente se você tiver adicionado um idioma que contém caracteres asiáticos ou de script complexo, na caixa de diálogo **Preferências de idioma do Microsoft Office** . (Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.
  
O número 0 (zero) significa que nenhuma fonte for especificada. A fonte latina ou fontes padrão são usadas.
  
Para obter uma referência para a célula ComplexScriptFont pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.ComplexScriptFont [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula ComplexScriptFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

