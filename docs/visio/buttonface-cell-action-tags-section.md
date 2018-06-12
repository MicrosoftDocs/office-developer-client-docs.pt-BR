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
description: Contém a identificação da imagem da face do botão exibido no botão de marca de ação.
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771430"
---
# <a name="buttonface-cell-action-tags-section"></a>Célula ButtonFace (Seção Action Tags)

Contém a identificação da imagem da face do botão exibido no botão de marca de ação. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

A cadeia de caracteres contida na célula ButtonFace representa a identificação de uma imagem de face de botão do Microsoft Office. Um valor 0 (zero) ou deixe em branco, por padrão, o botão de informações de "i" de marca de ação padrão ![](media/InfoPS_ZA10180114.gif).
  
As IDs que podem ser usadas na célula ButtonFace são os mesmos as IDs usadas com a propriedade **FaceID** de um objeto **CommandBarButton** . Para obter mais detalhes sobre essas IDs, procure "Trabalhando com imagens de botão de barra de comandos" no MSDN. 
  
Para obter uma referência à célula ButtonFace pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . ButtonFace onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para obter uma referência à célula ButtonFace pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagButtonFace** <br/> |
   

