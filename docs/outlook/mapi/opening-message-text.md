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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348577"
---
# <a name="opening-message-text"></a>Abrir texto da mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O texto de uma mensagem é armazenado em sua propriedade **Body\_de PR** ou **PR\_propriedade\_compactada de RTF** . Para obter mais informações, **consulte\_PR Body** ([PidTagBody](pidtagbody-canonical-property.md)) **,\_PR HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) e **PR\_RTF\_compactado** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Se você oferecer suporte ao formato Rich Text (RTF), **abra\_PR RTF_COMPRESSED**. Se você não oferecer suporte a RTF, **abra\_PR Body**. Como o texto de uma mensagem pode ser grande, independentemente de estar ou não formatado, use **IMAPIProp:: OpenProperty** para abrir essas propriedades. Para obter mais informações, consulte [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Para exibir o texto da mensagem formatada
  
1. Se você estiver usando um repositório de mensagens com reconhecimento não RTF, conforme indicado pela ausência do sinalizador STORE_RTF_OK na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da loja:
    
    1. Chame o método **IMAPIProp::** GetProps da mensagem para recuperar a propriedade **PR_RTF_IN_SYNC** . Para obter mais informações, consulte [IMAPIProp::](imapiprop-getprops.md) GetProps e **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Chame RTFSync para sincronizar a propriedade PR_BODY da mensagem com a propriedade **PR_RTF_COMPRESSED** . Para obter mais informações, consulte [RTFSync](rtfsync.md), **PR_BODY**e **PR_RTF_COMPRESSED**. Passe o sinalizador RTF_SYNC_BODY_CHANGED se a chamada para recuperar o **PR_RTF_IN_SYNC** falhou porque a propriedade não existe ou está definida como false. 
        
    3. Se **RTFSync** retornou True — indicando que as alterações foram feitas, chame o método **IMAPIProp:: SaveChanges** da mensagem para armazená-las permanentemente. Para obter mais informações, consulte [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
2. Independentemente de você estar usando ou não um repositório de mensagens com reconhecimento de RTF:
    
    1. Chame **IMAPIProp:: OpenProperty** para abrir a propriedade **PR_RTF_COMPRESSED** . Para obter mais informações, consulte [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.
        
    2. Se **PR_RTF_COMPRESSED** não estiver disponível, chame **OpenProperty** para abrir a propriedade **PR_BODY** . 
        
    3. Chame a função **WrapCompressedRTFStream** para criar uma versão descompactado dos dados RTF compactados, se disponível. Para obter mais informações, consulte [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copie o texto formatado do fluxo para o local apropriado no formulário de mensagem. 
    
### <a name="to-display-plain-message-text"></a>Para exibir texto de mensagem simples
  
1. Chame o método **IMAPIProp::** GetProps da mensagem para recuperar a propriedade **PR_BODY** . Para obter mais informações, consulte [IMAPIProp::](imapiprop-getprops.md)GetProps.
    
2. Se **** GetProps retornar PT_ERROR para o tipo de propriedade na estrutura de valor da propriedade ou MAPI_E_NOT_ENOUGH_MEMORY, chame o método **IMAPIProp:: OpenProperty** da mensagem. Passe **PR_BODY** como a marca de propriedade e IID_IStream como o identificador de interface. Para obter mais informações, consulte [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).
    
3. Copie o texto sem formatação do fluxo para o local apropriado no formulário de mensagem. 
    

