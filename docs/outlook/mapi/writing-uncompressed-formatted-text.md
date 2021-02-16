---
title: Escrevendo texto formatado descompactado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426321"
---
# <a name="writing-uncompressed-formatted-text"></a>Escrevendo texto formatado descompactado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao se preparar para enviar uma mensagem com texto formatado, de definir a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)da mensagem como texto compactado ou descompactado. Escrever texto compactado na propriedade **PR_RTF_COMPRESSED** é uma operação muito intensa da CPU e pode afetar significativamente o desempenho. 
  
Para melhorar o desempenho do envio de mensagens formatadas:
  
- Atualize a CPU, uma solução que nem sempre é um problema.
    
    - Ou -
    
- Escreva texto descompactado na **PR_RTF_COMPRESSED** propriedade. 
    
O procedimento para definir **PR_RTF_COMPRESSED** com texto descompactado é o mesmo para defini-lo com texto compactado, com uma exceção. Ao chamar [WrapCompressedRTFStream](wrapcompressedrtfstream.md), defina o STORE_UNCOMPRESSED_RTF no _parâmetro ulFlags._ Definir texto não compactado tem a desvantagem de aumentar o tamanho das mensagens. 
  

