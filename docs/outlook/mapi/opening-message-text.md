---
title: Abrir texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407533"
---
# <a name="opening-message-text"></a>Abrir texto da mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O texto de uma mensagem é armazenado em sua **propriedade PR \_ BODY** ou **PR \_ RTF \_ COMPRESSED.** Para obter mais informações, consulte **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) e **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Se você tiver suporte para Rich Text Format (RTF), abra **o formato PR \_ RTF_COMPRESSED**. Se você não tiver suporte para RTF, abra **PR \_ BODY**. Como o texto de uma mensagem pode ser grande independentemente de estar ou não formatado, use **IMAPIProp::OpenProperty** para abrir essas propriedades. Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Para exibir texto de mensagem formatado
  
1. Se você estiver usando um repositório de mensagens que não reconhece RTF, conforme indicado pela ausência do sinalizador STORE_RTF_OK na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório:
    
    1. Chame o método **IMAPIProp::GetProps** da mensagem para recuperar a **PR_RTF_IN_SYNC** propriedade. Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md) e **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Chame RTFSync para sincronizar a propriedade PR_BODY mensagem com a **PR_RTF_COMPRESSED** propriedade. Para obter mais informações, [consulte RTFSync,](rtfsync.md) **PR_BODY** e **PR_RTF_COMPRESSED**. Passe o RTF_SYNC_BODY_CHANGED sinalizador se a chamada para recuperar PR_RTF_IN_SYNC **falhou** porque a propriedade não existe ou está definida como FALSE. 
        
    3. Se **RTFSync** retornou TRUE indicando que as alterações foram feitas, chame o método **IMAPIProp::SaveChanges** da mensagem para armazená-las permanentemente. Para obter mais informações, [consulte IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Independentemente de você estar ou não usando um armazenamento de mensagens com conhecimento RTF:
    
    1. Chame **IMAPIProp::OpenProperty** para abrir **a** PR_RTF_COMPRESSED propriedade. Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.
        
    2. Se **PR_RTF_COMPRESSED** não estiver disponível, chame **OpenProperty** para abrir a **PR_BODY** propriedade. 
        
    3. Chame a **função WrapCompressedRTFStream** para criar uma versão descompactada dos dados RTF compactados, se disponível. Para obter mais informações, [consulte WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copie o texto formatado do fluxo para o local apropriado no formulário de mensagem. 
    
### <a name="to-display-plain-message-text"></a>Para exibir texto de mensagem simples
  
1. Chame o método **IMAPIProp::GetProps** da mensagem para recuperar a **PR_BODY** propriedade. Para obter mais informações, [consulte IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Se **GetProps** retornar PT_ERROR para o tipo de propriedade na estrutura de valores da propriedade ou MAPI_E_NOT_ENOUGH_MEMORY, chame o método **IMAPIProp::OpenProperty** da mensagem. Passe **PR_BODY** como a marca de propriedade e IID_IStream como o identificador da interface. Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copie o texto simples do fluxo para o local apropriado no formulário de mensagem. 
    

