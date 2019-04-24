---
title: Adicionar informações de renderização ao texto formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331119"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Adicionar informações de renderização ao texto formatado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para indicar o local no texto formatado onde um anexo é renderizado, você deve inserir uma sequência de caracteres de espaço reservado na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem. A sequência de espaço reservado é composta pelos seguintes caracteres: `\objattph`.
  
 **Para adicionar informações de renderização ao texto da mensagem formatada**
  
- Ao gravar o fluxo de texto na propriedade **PR_RTF_COMPRESSED** da mensagem, insira a sequência de espaço reservado e um caractere de espaço na posição onde o anexo deve ser renderizado. 
    
- Defina a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada anexo como um valor numérico. O valor mais baixo deve ser atribuído à propriedade **PR_RENDERING_POSITION** do primeiro anexo a ser exibido no texto formatado; o valor mais alto para o último anexo. 
    

