---
title: Suporte a texto formatado em mensagens de saída responsabilidades do cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327402"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Suporte a texto formatado em mensagens de saída: responsabilidades do cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente definem a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou a propriedade **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para uma mensagem de saída. Os clientes que oferecem suporte somente a texto sem formatação só definem a propriedade **PR_BODY** . Os clientes cientes do formato Rich Text (RTF) podem definir as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** , ou apenas **PR_RTF_COMPRESSED**, dependendo do provedor de armazenamento de mensagens que está sendo usado. Clientes com reconhecimento de HTML definem a propriedade **PR_HTML** . 
  
É importante que um cliente Verifique sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório de mensagens para determinar se o repositório suporta RTF. Se o repositório de mensagens não reconhece o RTF, um cliente com reconhecimento de RTF define as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** para cada mensagem de saída. 
  
Se o repositório de mensagens tiver reconhecimento de RTF, somente a propriedade **PR_RTF_COMPRESSED** precisará ser definida. 
  
 **Para definir PR_RTF_COMPRESSED e garantir que o processo de sincronização ocorra conforme necessário, os clientes com reconhecimento de RTF**
  
1. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** , definindo os sinalizadores MAPI_CREATE e MAPI_MODIFY. O MAPI_CREATE garante que todos os novos dados substituam os dados antigos e o MAPI_MODIFY permite que você faça essas substituições. 
    
2. Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando STORE_UNCOMPRESSED_RTF se o repositório de mensagens define o bit STORE_UNCOMPRESSED_RTF em sua propriedade **PR_STORE_SUPPORT_MASK** , para obter uma versão descompactada do **PR_RTF_COMPRESSED **Stream retornado de **OpenProperty**.
    
3. Escreva os dados de texto da mensagem para o fluxo descompactado retornado de **WrapCompressedRTFStream**.
    
4. Confirmar e liberar os fluxos não compactados e compactados.
    
Neste ponto, se o provedor do repositório de mensagens oferecer suporte a RTF, tudo isso é necessário. Você pode depender do provedor de armazenamento de mensagens para lidar com o processo de sincronização e a criação da propriedade **PR_BODY** , se necessário. No enTanto, se o provedor do repositório de mensagens não oferecer suporte a RTF, você deverá chamar a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação, definindo o sinalizador RTF_SYNC_RTF_CHANGED. 
  

