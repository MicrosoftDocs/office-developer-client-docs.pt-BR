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
ms.openlocfilehash: a6018c05d1191211242066425e4ae546c1618094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594555"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Adicionar informações de renderização ao texto formatado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para indicar o local no texto formatado em que um anexo é processado, você deve inserir uma sequência de caracteres de espaço reservado na propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem. A sequência de espaço reservado é composta pelos seguintes caracteres: `\objattph`.
  
 **Para adicionar informações de renderização ao texto da mensagem formatada**
  
- Ao escrever o fluxo de texto à propriedade **PR_RTF_COMPRESSED** da mensagem, insira a sequência de espaço reservado e um caractere de espaço na posição onde o anexo deve ser processado. 
    
- Defina a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de cada anexo para um valor numérico. O menor valor deve ser atribuído à propriedade **PR_RENDERING_POSITION** do primeiro anexo seja exibido em texto formatado; o valor mais alto para o último anexo. 
    

