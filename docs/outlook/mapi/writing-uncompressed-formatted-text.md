---
title: Gravar texto formatado sem compactação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325750"
---
# <a name="writing-uncompressed-formatted-text"></a>Gravar texto formatado sem compactação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao se preparar para enviar uma mensagem com texto formatado, defina a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem como texto compactado ou descompactado. A gravação de texto compactado na propriedade **PR_RTF_COMPRESSED** é uma operação muito intensa da CPU e pode afetar seriamente o desempenho. 
  
Para melhorar o desempenho do envio de mensagens formatadas, você pode:
  
- Atualize a CPU, uma solução que nem sempre é plausível.
    
    - Ou
    
- Escreva texto descompactado na propriedade **PR_RTF_COMPRESSED** . 
    
O procedimento para configurar **PR_RTF_COMPRESSED** com texto descompactado é o mesmo que para configurá-lo com texto compactado, com uma exceção. Ao chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md), defina o sinalizador STORE_UNCOMPRESSED_RTF no parâmetro _parâmetroulflags_ . A configuração do texto descompactado tem a desvantagem de que aumenta o tamanho das mensagens. 
  

