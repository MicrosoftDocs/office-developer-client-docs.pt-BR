---
title: Célula ButtonFace (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771429"
---
# <a name="buttonface-cell-actions-section"></a>Célula ButtonFace (Seção Actions)

Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

A sequência de caracteres contida na célula ButtonFace representa a ID de uma imagem de face do botão do Microsoft Office. Um valor zero (0) ou em branco significa que nenhum ícone é exibido. 
  
As IDs que podem ser usadas na célula ButtonFace são os mesmos as IDs usadas com a propriedade **FaceID** de um objeto **CommandBarButton** . Para obter mais detalhes sobre essas IDs, procure "Trabalhando com imagens de botão de barra de comandos" no MSDN. 
  
Para obter uma referência para a célula ButtonFace pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |**Ações**.  *nome* . **ButtonFace** onde **ações**.  *nome* é o nome da linha actions  <br/> |
   
Para fazer referência à célula ButtonFace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde **i** = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionButtonFace** <br/> |
   

