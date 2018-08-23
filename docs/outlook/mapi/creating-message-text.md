---
title: Criando o texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bd840c7bef0607db37c6477bd8f4a7320a8188c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574752"
---
# <a name="creating-message-text"></a>Criando o texto da mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Embora algumas mensagens são compostas de nada mais que uma lista de destinatários e uma linha de assunto, o conteúdo da maioria das mensagens, especificamente IPM. Observação as mensagens, inclui o texto. Mensagem de texto pode ser simples ou formatada e está armazenado em três propriedades: **PR\_corpo** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Se seu cliente é baseado em texto sem formatação, defina **PR\_corpo**. Caso você ofereça suporte texto formatado em Rich Text Format (RTF), definidos **PR_RTF_COMPRESSED** apenas ou ambos os **PR_RTF_COMPRESSED** e **PR\_corpo**, dependendo do provedor de armazenamento de mensagem que você está usando. Quando um cliente RTF reconhecimento estiver usando um armazenamento de mensagens RTF reconhecimento, ela define **PR_RTF_COMPRESSED** somente. Quando um cliente RTF reconhecimento estiver usando um armazenamento de mensagens sem reconhecimento de RTF, ela define ambas as propriedades. Se seu cliente ofereça suporte a HTML, defina a propriedade **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Determinar se o seu armazenamento de mensagens suporta formato Rich Text
  
1. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Verifique se o bit STORE_RTF_OK. Se STORE_RTF_OK for definido, o provedor de armazenamento de mensagem suporta texto RTF. Se não estiver definida, o provedor de armazenamento de mensagem suporta apenas texto sem formatação.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Determinar se o seu armazenamento de mensagens oferece suporte a HTML
  
1. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_STORE_SUPPORT_MASK** . 
    
2. Verifique se o bit STORE_HTML_OK. Se STORE_HTML_OK for definido, o provedor de armazenamento de mensagem suporta texto HTML. 
    
## <a name="set-prrtfcompressed"></a>Definir PR\_RTF_COMPRESSED
  
1. Chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da mensagem para abrir a propriedade **PR_RTF_COMPRESSED** , especificando IID_IStream como o identificador de interface e definindo o sinalizador MAPI_CREATE. 
    
2. Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando o sinalizador STORE_UNCOMPRESSED_RTF se o bit STORE_UNCOMPRESSED_RTF é definido na propriedade **PR_STORE_SUPPORT_MASK** do armazenamento de mensagens. 
    
3. Liberar o fluxo original chamando seu * * IUnknown:: Release * * método. 
    
4. Chamar tanto * * IStream::Write * * ou **IStream::CopyTo** para gravar o fluxo de texto da mensagem retornado da **WrapCompressedRTFStream**.
    
5. Chame os métodos **Commit** e a **versão** no fluxo retornado pelo método **OpenProperty** . 
    
Neste ponto, se o provedor de armazenamento de mensagem suporta RTF, você fez tudo o que é necessário. Você pode depender o provedor de armazenamento de mensagem para lidar com formatação e sincronizando conteúdo da mensagem e criar o **PR\_corpo** propriedade, se necessário. Repositórios de mensagem RTF reconhecimento chame [RTFSync](rtfsync.md) para lidar com a sincronização. Se o RTF\_sinalizador SYNC_BODY_CHANGED é definido como TRUE, o provedor será recompilar a propriedade **PR_BODY** . 
  
Se o seu provedor de armazenamento de mensagens não oferece suporte a RTF, você também deve adicionar o conteúdo da mensagem não-RTF, definindo a propriedade **PR_BODY** . 
  
## <a name="set-prhtml"></a>Definir PR_HTML
  
1. Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_HTML** com a interface **IStream** . 
    
2. Chame **IStream::Write** para gravar os dados de texto de mensagem no fluxo retornado da **OpenProperty**. 
    
3. Chamadas **IStream::Commit** e **IUnknown:: Release** no fluxo para confirmar as alterações e liberar sua memória. 
    
## <a name="set-prbody"></a>Definir PR_BODY
  
1. Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_BODY** com a interface **IStream** . 
    
2. Chame **IStream::Write** para gravar os dados de texto de mensagem no fluxo retornado da **OpenProperty**. 
    
3. Chame a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação. Como esta é uma nova mensagem, defina o RTF_SYNC_RTF_CHANGED e o RTF_SYNC_BODY_CHANGED sinalizadores para indicar que a versão RTF tanto o texto sem formatação do texto da mensagem foi alterado. **RTFSync** irá definir várias propriedades relacionadas que requer que o provedor de armazenamento de mensagens, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e gravá-los à mensagem.
    
4. Chamadas **IStream::Commit** e **IUnknown:: Release** no fluxo para confirmar as alterações e liberar sua memória. 
    

