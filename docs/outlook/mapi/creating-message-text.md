---
title: Criar texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428001"
---
# <a name="creating-message-text"></a>Criar texto da mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Embora algumas mensagens sejam formadas por nada além de uma lista de destinatários e uma linha de assunto, o conteúdo da maioria das mensagens, especificamente IPM. Mensagens de observação, incluindo texto. O texto da mensagem pode ser simples ou formatado e é armazenado em três propriedades: **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Se o cliente for baseado em texto sem formatação, **defina\_PR Body**. Se você oferecer suporte ao texto formatado no formato Rich Text (RTF), defina **PR_RTF_COMPRESSED** somente ou ambos **PR_RTF_COMPRESSED** e **PR\_corpo**, dependendo do provedor de repositório de mensagens que você está usando. Quando um cliente com reconhecimento de RTF está usando um repositório de mensagens com reconhecimento de RTF, ele define **PR_RTF_COMPRESSED** somente. Quando um cliente com reconhecimento de RTF está usando um repositório de mensagens que não reconhece RTF, ele define ambas as propriedades. Se o cliente oferecer suporte a HTML, defina a propriedade **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Determinar se o repositório de mensagens suporta o formato Rich Text
  
1. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Verifique o bit STORE_RTF_OK. Se STORE_RTF_OK estiver definido, o provedor de armazenamento de mensagens oferece suporte a texto RTF. Se ele não estiver definido, o provedor do repositório de mensagens só oferece suporte a texto sem formatação.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Determinar se o repositório de mensagens oferece suporte a HTML
  
1. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar a propriedade **PR_STORE_SUPPORT_MASK** . 
    
2. Verifique o bit STORE_HTML_OK. Se STORE_HTML_OK estiver definido, o provedor de armazenamento de mensagens oferece suporte a texto HTML. 
    
## <a name="set-prrtfcompressed"></a>Set PR\_RTF_COMPRESSED
  
1. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) da mensagem para abrir a propriedade **PR_RTF_COMPRESSED** , especificando IID_IStream como o identificador de interface e definindo o sinalizador MAPI_CREATE. 
    
2. Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando o sinalizador STORE_UNCOMPRESSED_RTF se o bit STORE_UNCOMPRESSED_RTF estiver definido na propriedade **PR_STORE_SUPPORT_MASK** do repositório de mensagens. 
    
3. Libere o fluxo original chamando seu método * * IUnknown:: Release * *. 
    
4. Call * * IStream:: Write * * ou **IStream:: CopyTo** para gravar o texto da mensagem no Stream retornado por **WrapCompressedRTFStream**.
    
5. Chame os métodos **Commit** e **Release** no Stream retornado do método **OpenProperty** . 
    
Neste ponto, se o provedor do repositório de mensagens oferecer suporte a RTF, tudo isso é necessário. Você pode depender do provedor de armazenamento de mensagens para lidar com a sincronização do conteúdo e da formatação da mensagem e criar a propriedade do **corpo da pr\_** , se necessário. O armazenamento de mensagens com reconhecimento de RTF chama [RTFSync](rtfsync.md) para lidar com a sincronização. Se o sinalizador\_RTF SYNC_BODY_CHANGED for definido como true, o provedor recalculará a propriedade **PR_BODY** . 
  
Se o seu provedor de repositório de mensagens não oferecer suporte a RTF, você também deve adicionar conteúdo de mensagem não-RTF, definindo a propriedade **PR_BODY** . 
  
## <a name="set-prhtml"></a>Definir PR_HTML
  
1. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_HTML** com a interface **IStream** . 
    
2. IStream de chamada **:: Write** para gravar os dados de texto da mensagem no Stream retornado de **OpenProperty**. 
    
3. IStream de chamada **:: Commit** e **IUnknown:: Release** no Stream para confirmar as alterações e liberar a memória. 
    
## <a name="set-prbody"></a>Definir PR_BODY
  
1. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_BODY** com a interface **IStream** . 
    
2. IStream de chamada **:: Write** para gravar os dados de texto da mensagem no Stream retornado de **OpenProperty**. 
    
3. Chame a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação. Como esta é uma nova mensagem, defina os sinalizadores RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED para indicar que a versão RTF e de texto sem formatação do texto da mensagem foi alterada. **RTFSync** definirá várias propriedades relacionadas que o provedor de armazenamento de mensagens requer, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), e gravá-las na mensagem.
    
4. IStream de chamada **:: Commit** e **IUnknown:: Release** no Stream para confirmar as alterações e liberar a memória. 
    

