---
title: Célula ButtonFace (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contém a ID da imagem de face do botão que é exibida no botão de marca de ação.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337532"
---
# <a name="buttonface-cell-action-tags-section"></a>Célula ButtonFace (Seção Action Tags)

Contém a ID da imagem de face do botão que é exibida no botão de marca de ação. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

.A cadeia de caracteres contida na célula ButtonFace representa a identificação de uma imagem de face do botão do Microsoft Office. Um valor 0 (zero) ou em branco assume como padrão o botão de informação "i" da marca de ação ![Botão de informação"i" da marca de ação padrão](media/InfoPS_ZA10180114.gif).
  
As identificações que podem ser usadas na célula ButtonFace são as mesmas que as utilizadas com a propriedade **FaceID** de um objeto **CommandBarButton**. Para obter mais detalhes sobre essas identificações, procure "trabalhando com imagens de botão da barra de comandos" na MSDN. 
  
Para obter uma referência à célula ButtonFace pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *name*  .ButtonFace           em que SmartTags. *name*  é o nome da linha da marca de ação  <br/> |
   
Para obter uma referência à célula ButtonFace pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visSmartTagButtonFace** <br/> |
   

