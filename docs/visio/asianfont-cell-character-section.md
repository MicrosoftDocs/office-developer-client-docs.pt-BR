---
title: Célula AsianFont (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contém o número da fonte utilizada para formatar o texto com caracteres asiáticos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341326"
---
# <a name="asianfont-cell-character-section"></a>Célula AsianFont (Seção Character)

Contém o número da fonte utilizada para formatar o texto com caracteres asiáticos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. 
  
## <a name="remarks"></a>Comentários

Fontes asiáticas são listadas na guia **Fonte** na caixa de diálogo **Texto** (clique na seta do grupo **Fonte** na guia **Página Inicial**). Essa lista só é exibida se você tiver adicionado um idioma que contenha caracteres Asiáticos ou de script complexo, na caixa de diálogo **Preferências de Idioma do Microsoft Office**. (Clique em **Iniciar**, em **Todos os programas**, em **Microsoft Office**, em **Ferramentas do Microsoft Office** e em **Preferências de Idioma do Microsoft Office**.
  
O número 0 significa que não há fontes especificadas. A fonte latina ou as fontes padrão são usadas se elas contiverem os caracteres necessários.
  
Para fazer referência à célula AsianFont pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char. AsianFont [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula AsianFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterAsianFont** <br/> |
   

