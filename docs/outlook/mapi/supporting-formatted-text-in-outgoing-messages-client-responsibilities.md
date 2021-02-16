---
title: Suporte a texto formatado em responsabilidades do cliente de mensagens de saída
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431600"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Suporte a texto formatado em mensagens de saída: responsabilidades do cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente configuram a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou a propriedade **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para uma mensagem de saída. Clientes que suportam apenas texto sem texto definido apenas **PR_BODY** propriedade. Clientes com conhecimento em RTF (Rich Text Format) podem definir as propriedades **PR_BODY** e **PR_RTF_COMPRESSED,** ou apenas **PR_RTF_COMPRESSED,** dependendo do provedor de armazenamento de mensagens que está sendo usado. Os clientes com suporte a HTML configuram **a PR_HTML** propriedade. 
  
É importante que um cliente verifique a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)do repositório de mensagens para determinar se o repositório oferece suporte a RTF. Se o armazenamento de mensagens não estiver ciente de RTF, um cliente que reconhece RTF define as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** para cada mensagem de saída. 
  
Se o armazenamento de mensagens for ciente de RTF, somente a PR_RTF_COMPRESSED **propriedade** precisará ser definida. 
  
 **Para definir PR_RTF_COMPRESSED e garantir que o processo de sincronização ocorra conforme necessário, clientes com conhecimento RTF**
  
1. Chame o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED,** definindo os sinalizadores MAPI_CREATE e MAPI_MODIFY padrão. MAPI_CREATE garante que os novos dados substituam todos os dados antigos e MAPI_MODIFY que você faça essas substituições. 
    
2. Chame a função [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) passando STORE_UNCOMPRESSED_RTF se o armazenamento de mensagens define o bit STORE_UNCOMPRESSED_RTF em sua propriedade **PR_STORE_SUPPORT_MASK,** para obter uma versão descompactada do fluxo **PR_RTF_COMPRESSED** retornado de **OpenProperty**.
    
3. Gravar os dados de texto da mensagem no fluxo descompactado retornado de **WrapCompressedRTFStream**.
    
4. Confirma e libera os fluxos descompactados e compactados.
    
Neste ponto, se o provedor de armazenamento de mensagens suportar RTF, você fez tudo o que é necessário. Você pode depender do provedor do armazenamento de mensagens para manipular o processo de sincronização e a criação da **PR_BODY,** se necessário. No entanto, se o provedor de armazenamento de mensagens não suportar RTF, você deverá chamar a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação, definindo o sinalizador de RTF_SYNC_RTF_CHANGED. 
  

