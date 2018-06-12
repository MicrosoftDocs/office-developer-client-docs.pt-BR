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
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771270"
---
# <a name="asianfont-cell-character-section"></a>Célula AsianFont (Seção Character)

Contém o número da fonte utilizada para formatar o texto com caracteres asiáticos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema. 
  
## <a name="remarks"></a>Comentários

Fontes para idiomas asiáticos são listadas na guia **fonte** da caixa de diálogo **texto** (clique na seta na **fonte** de grupo na guia **página inicial** ). Esta lista é exibida somente se você tiver adicionado um idioma que contém caracteres asiáticos ou de script complexo, na caixa de diálogo **Preferências de idioma do Microsoft Office** . (Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.
  
O número 0 significa que não há fontes especificadas. A fonte latina ou as fontes padrão são usadas se elas contiverem os caracteres necessários.
  
Para obter uma referência à célula AsianFont pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.AsianFont [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula AsianFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterAsianFont** <br/> |
   

