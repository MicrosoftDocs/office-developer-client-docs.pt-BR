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
description: Identifica o ícone exibido ao lado de um item em um menu de atalho ou de marca de ação.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407372"
---
# <a name="buttonface-cell-actions-section"></a>Célula ButtonFace (Seção Actions)

Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

A sequência de caracteres contida na célula ButtonFace representa a ID de uma imagem de face do botão do Microsoft Office. Um valor zero (0) ou em branco significa que nenhum ícone é exibido. 
  
As identificações que podem ser usadas na célula ButtonFace são as mesmas que as utilizadas com a propriedade **FaceID** de um objeto **CommandBarButton**. Para obter mais detalhes sobre essas identificações, procure "trabalhando com imagens de botão da barra de comandos" na MSDN. 
  
Para obter uma referência para a célula ButtonFace pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |**Ações**.  *nome* . **ButtonFace** onde **Actions**.  *Name* é o nome da linha de ações  <br/> |
   
Para fazer referência à célula ButtonFace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice de linha:  <br/> |**visRowAction** +  *i* onde **i** = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionButtonFace** <br/> |
   

