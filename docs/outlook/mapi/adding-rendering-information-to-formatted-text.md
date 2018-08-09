---
title: Adicionar informações de renderização ao texto formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766134"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Adicionar informações de renderização ao texto formatado

  
  
**Aplica-se a**: Outlook 
  
Para indicar o local no texto formatado em que um anexo é processado, você deve inserir uma sequência de caracteres de espaço reservado na propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem. A sequência de espaço reservado é composta pelos seguintes caracteres: `\objattph`.
  
 **Para adicionar informações de renderização ao texto da mensagem formatada**
  
- Ao escrever o fluxo de texto à propriedade **PR_RTF_COMPRESSED** da mensagem, insira a sequência de espaço reservado e um caractere de espaço na posição onde o anexo deve ser processado. 
    
- Defina a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada anexo para um valor numérico. O menor valor deve ser atribuído à propriedade **PR_RENDERING_POSITION** do primeiro anexo seja exibido em texto formatado; o valor mais alto para o último anexo. 
    

