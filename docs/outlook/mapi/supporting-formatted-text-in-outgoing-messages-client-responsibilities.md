---
title: Suporte de texto formatado em saída responsabilidades de cliente de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770519"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Suporte a texto formatado em mensagens de saída: responsabilidades do cliente

  
  
**Aplica-se a**: Outlook 
  
Aplicativos cliente defina a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou a propriedade **PR_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) para uma mensagem de saída. Clientes com suporte apenas texto sem formatação definida apenas a propriedade **PR_BODY** . Formato Rich Text (RTF)-lembre-se os clientes podem definir ambas as propriedades **PR_RTF_COMPRESSED** e **PR_BODY** , ou apenas **PR_RTF_COMPRESSED**, dependendo da mensagem armazenar provedor que está sendo usado. Clientes de HTML defina a propriedade **PR_HTML** . 
  
É importante para um cliente verificar a propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do seu armazenamento de mensagens para determinar se o repositório suporta RTF. Se o armazenamento de mensagens não for RTF reconhecimento, um cliente de reconhecimento de RTF define propriedades **PR_BODY** tanto o **PR_RTF_COMPRESSED** para cada mensagem de saída. 
  
Se o armazenamento da mensagem for RTF reconhecimento, apenas a propriedade **PR_RTF_COMPRESSED** deve ser definido. 
  
 **Para definir PR_RTF_COMPRESSED e certifique-se de que a sincronização processo ocorre à medida que os clientes necessários, reconhecimento de RTF**
  
1. Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** , definindo sinalizadores MAPI_CREATE tanto o MAPI_MODIFY. MAPI_CREATE garante que todos os dados novos substituem quaisquer dados antigos e MAPI_MODIFY permite que você faça as substituições. 
    
2. Chamar a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando STORE_UNCOMPRESSED_RTF se o armazenamento de mensagens define estará definido o bit STORE_UNCOMPRESSED_RTF em sua propriedade **PR_STORE_SUPPORT_MASK** , para obter uma versão descompactada do **PR_RTF_COMPRESSED **stream retornado da **OpenProperty**.
    
3. Gravar os dados de texto de mensagem no fluxo descompactado retornado da **WrapCompressedRTFStream**.
    
4. Confirmar e versão fluxos compactados e descompactados.
    
Neste ponto, se o provedor de armazenamento de mensagem suporta RTF, você fez tudo o que é necessário. Você pode depender o provedor de armazenamento de mensagem para lidar com o processo de sincronização e a criação da propriedade **PR_BODY** , se necessário. No entanto, se o provedor de armazenamento de mensagens não oferece suporte a RTF, você deve chamar a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação, definindo o sinalizador RTF_SYNC_RTF_CHANGED. 
  

