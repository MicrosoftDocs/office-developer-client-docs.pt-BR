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
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404831"
---
# <a name="complexscriptfont-cell-character-section"></a>Célula ComplexScriptFont (Seção Caractere)

Contém o número da fonte utilizada para formatar o texto composto de caracteres de script complexos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. 
  
## <a name="remarks"></a>Comentários

Tamanhos de fonte de script complexos são listados na guia **Fonte** na caixa de diálogo **Texto** (clique na seta no grupo **Fonte** na guia **Início**). Essa lista só é exibida se você tiver adicionado um idioma que contenha caracteres Asiáticos ou de script complexo, na caixa de diálogo **Preferências de Idioma do Microsoft Office**. (Clique em **Iniciar**, em **Todos os programas**, em **Microsoft Office**, em **Ferramentas do Microsoft Office** e em **Preferências de Idioma do Microsoft Office**.
  
O número 0 (zero) significa que não há fontes especificadas. A fonte latina ou fontes padrão são usadas.
  
Para obter uma referência à célula ComplexScriptSize pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.ComplexScriptFont[ *i*  ]           onde  *i*  = <1>, 2, 3...  <br/> |
   
Para obter uma referência à célula ComplexScriptFont pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice de linha:  <br/> |**visRowCharacter** +  *i*           onde  *i*  = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

