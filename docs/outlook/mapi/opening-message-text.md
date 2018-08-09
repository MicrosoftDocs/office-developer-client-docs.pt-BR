---
title: Texto da mensagem de abertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768181"
---
# <a name="opening-message-text"></a>Texto da mensagem de abertura

**Aplica-se a**: Outlook 
  
O texto de uma mensagem é armazenado no seu **PR\_corpo** propriedade ou **PR\_RTF\_COMPRESSED** propriedade. Para obter mais informações, consulte **PR\_corpo** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) e **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Caso você ofereça suporte a Rich Text Format (RTF), abra **PR\_RTF_COMPRESSED**. Se você não suportam RTF, abra **PR\_corpo**. Como o texto de uma mensagem pode ser grande, independentemente de estarem ou não está formatado, use **IMAPIProp::OpenProperty** para abrir essas propriedades. Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Para exibir o texto de mensagem de formatado
  
1. Se você estiver usando um armazenamento de mensagens de reconhecimento de não-RTF, conforme indicado pela ausência do sinalizador STORE_RTF_OK na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da loja:
    
    1. Chame o método de **IMAPIProp::GetProps** da mensagem para recuperar a propriedade **PR_RTF_IN_SYNC** . Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md) e **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Chame RTFSync para sincronizar a propriedade PR_BODY da mensagem com a propriedade **PR_RTF_COMPRESSED** . Para obter mais informações, consulte [RTFSync](rtfsync.md), **PR_BODY**e **PR_RTF_COMPRESSED**. PASS o RTF_SYNC_BODY_CHANGED sinalizar se a chamada para recuperar **PR_RTF_IN_SYNC** falhou porque a propriedade não existe ou ela é definida como FALSE. 
        
    3. Se **RTFSync** retornado TRUE — indicando que as alterações foram feitas — chamar o método de **IMAPIProp::SaveChanges** da mensagem para permanentemente armazená-los. Para obter mais informações, consulte [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Independentemente de estarem ou não estiver usando uma mensagem RTF reconhecimento armazene:
    
    1. Chame **IMAPIProp::OpenProperty** para abrir a propriedade **PR_RTF_COMPRESSED** . Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.
        
    2. Se **PR_RTF_COMPRESSED** não estiver disponível, chame **OpenProperty** para abrir a propriedade **PR_BODY** . 
        
    3. Chame a função de **WrapCompressedRTFStream** para criar uma versão descompactada dos dados compactados RTF, se disponível. Para obter mais informações, consulte [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copie o texto formatado do stream até o local apropriado no formulário da mensagem. 
    
### <a name="to-display-plain-message-text"></a>Para exibir texto sem formatação de mensagem
  
1. Chame o método de **IMAPIProp::GetProps** da mensagem para recuperar a propriedade **PR_BODY** . Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Se **GetProps** retornar qualquer PT_ERROR o tipo de propriedade na estrutura do valor de propriedade ou MAPI_E_NOT_ENOUGH_MEMORY, chame o método de **IMAPIProp::OpenProperty** da mensagem. Passe **PR_BODY** como a marca de propriedade e IID_IStream como o identificador de interface. Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copie o texto sem formatação do stream até o local apropriado no formulário da mensagem. 
    

