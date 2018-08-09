---
title: Gravar texto formatado sem compactação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770738"
---
# <a name="writing-uncompressed-formatted-text"></a>Gravar texto formatado sem compactação

  
  
**Aplica-se a**: Outlook 
  
Durante a preparação enviar uma mensagem com o texto formatado, tanto definir a propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem como texto compactado ou descompactado. Gravar texto compactado na propriedade **PR_RTF_COMPRESSED** é uma operação intensiva na CPU exato e pode afetar significativamente o desempenho. 
  
Para melhorar o desempenho do envio de mensagens formatadas, seja:
  
- Atualize a CPU, uma solução que nem sempre é plausível.
    
    - Ou -
    
- Escreva o texto descompactado na propriedade **PR_RTF_COMPRESSED** . 
    
O procedimento para definir **PR_RTF_COMPRESSED** com texto descompactado é a mesma que para defini-la com texto compactado, com uma exceção. Ao chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md), defina o sinalizador STORE_UNCOMPRESSED_RTF no parâmetro _ulFlags_ . Definindo texto descompactado tem a desvantagem em que ela aumenta o tamanho das mensagens. 
  

