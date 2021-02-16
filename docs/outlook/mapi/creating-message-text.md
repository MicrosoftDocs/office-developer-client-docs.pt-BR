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
  
Embora algumas mensagens sejam feitas de nada mais do que uma lista de destinatários e uma linha de assunto, o conteúdo da maioria das mensagens, especificamente IPM. Anotações de mensagens, inclui texto. O texto da mensagem pode ser simples ou formatado e armazenado em três propriedades: **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Se seu cliente for baseado em texto sem texto, de definida **PR \_ BODY**. Se você tiver suporte para texto formatado no  Formato Rich Text  (RTF), de definida PR_RTF_COMPRESSED somente ou PR_RTF_COMPRESSED e **\_ PR BODY**, dependendo do provedor de armazenamento de mensagens que você estiver usando. Quando um cliente que reconhece RTF está usando um armazenamento de mensagens com conhecimento RTF, ele **define** PR_RTF_COMPRESSED somente. Quando um cliente que reconhece RTF está usando um armazenamento de mensagens que não reconhece RTF, ele define ambas as propriedades. Se o cliente for compatível com HTML, de definida **PR_HTML** propriedade. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Determinar se o armazenamento de mensagens é compatível com o Formato Rich Text
  
1. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do repositório de mensagens para recuperar a **propriedade PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Verifique o STORE_RTF_OK bit. Se STORE_RTF_OK for definido, o provedor de armazenamento de mensagens será compatível com texto RTF. Se não estiver definido, o provedor do armazenamento de mensagens oferece suporte somente a texto sem texto.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Determinar se o armazenamento de mensagens é compatível com HTML
  
1. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a **PR_STORE_SUPPORT_MASK** propriedade. 
    
2. Verifique o STORE_HTML_OK bit. Se STORE_HTML_OK for definido, o provedor de armazenamento de mensagens será compatível com texto HTML. 
    
## <a name="set-pr_rtf_compressed"></a>Definir configurações de \_ RTF_COMPRESSED
  
1. Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da mensagem para abrir a propriedade **PR_RTF_COMPRESSED,** especificando IID_IStream como o identificador da interface e definindo o sinalizador MAPI_CREATE. 
    
2. Chame a [função WrapCompressedRTFStream,](wrapcompressedrtfstream.md) passando o sinalizador STORE_UNCOMPRESSED_RTF se o bit STORE_UNCOMPRESSED_RTF estiver definido na propriedade PR_STORE_SUPPORT_MASK do armazenamento **de** mensagens. 
    
3. Libere o fluxo original chamando seu método ** IUnknown::Release **. 
    
4. Chame ** IStream::Write ** ou **IStream::CopyTo** para gravar o texto da mensagem no fluxo retornado de **WrapCompressedRTFStream**.
    
5. Chame os **métodos Commit** e **Release** no fluxo retornado do **método OpenProperty.** 
    
Neste ponto, se o provedor de armazenamento de mensagens suportar RTF, você fez tudo o que é necessário. Você pode depender do provedor do armazenamento de mensagens para lidar com a sincronização do conteúdo e a formatação da mensagem e para criar a **propriedade PR \_ BODY,** se necessário. Os armazenamentos de mensagens com conhecimento RTF chamam [RTFSync](rtfsync.md) para manipular a sincronização. Se o sinalizador SYNC_BODY_CHANGED RTF estiver definido como TRUE, o provedor \_ recompute a **PR_BODY** propriedade. 
  
Se seu provedor de armazenamento de mensagens não suporta RTF, você também deve adicionar conteúdo de mensagem não RTF definindo a **PR_BODY** propriedade. 
  
## <a name="set-pr_html"></a>Definir PR_HTML
  
1. Chame o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_HTML** com a interface **IStream.** 
    
2. Chame **IStream::Write** para gravar os dados de texto da mensagem no fluxo retornado de **OpenProperty**. 
    
3. Chame **IStream::Commit** e **IUnknown::Release** no fluxo para confirma as alterações e liberar sua memória. 
    
## <a name="set-pr_body"></a>Definir PR_BODY
  
1. Chame o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_BODY** com a interface **IStream.** 
    
2. Chame **IStream::Write** para gravar os dados de texto da mensagem no fluxo retornado de **OpenProperty**. 
    
3. Chame a [função RTFSync](rtfsync.md) para sincronizar o texto com a formatação. Como esta é uma nova mensagem, de definir os sinalizadores RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED para indicar que a versão RTF e a versão de texto sem alterações do texto da mensagem foram alteradas. **O RTFSync** definirá várias propriedades relacionadas que o provedor de armazenamento de mensagens exige, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), e as gravará na mensagem.
    
4. Chame **IStream::Commit** e **IUnknown::Release** no fluxo para confirma as alterações e liberar sua memória. 
    

