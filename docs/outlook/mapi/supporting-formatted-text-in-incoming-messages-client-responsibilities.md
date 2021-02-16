---
title: Suporte a texto formatado em responsabilidades do cliente de mensagens de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434498"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
À medida que as mensagens são transferidas entre sistemas de mensagens, o spooler MAPI garante que a formatação rich text permaneça sincronizada com o texto da mensagem. O spooler MAPI chama a função [RTFSync](rtfsync.md) de dentro de uma versão empacotada da mensagem que ele passa para o provedor de transporte. O provedor de transporte salva as alterações feitas na mensagem chamando o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e, em seguida, o encaminha para o novo destinatário. 
  
Quando o aplicativo cliente que reconhece RTF do destinatário abre a mensagem para exibir o texto, ele deve sincronizar o texto com a formatação e abrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), dependendo de qual propriedade está disponível.
  
 **Para abrir uma mensagem, clientes com conhecimento RTF**
  
1. Chame **RTFSync** para sincronizar o texto da mensagem com a formatação se o armazenamento de mensagens não estiver ciente de RTF. O RTF_SYNC_BODY_CHANGED sinalizador deve ser passado no parâmetro  _ulFlags_ se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver ausente ou definida como FALSE. Clientes que trabalham com armazenamentos de mensagens com conhecimento RTF não precisam fazer a chamada **RTFSync** porque o armazenamento de mensagens cuida disso. 
    
2. Chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) se o texto da mensagem tiver sido atualizado. 
    
3. Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir **a** PR_RTF_COMPRESSED propriedade. Se **PR_RTF_COMPRESSED** não estiver disponível, você deve abrir a propriedade **PR_BODY** para exibir o conteúdo da mensagem. 
    
4. Chame a [função WrapCompressedRTFStream](wrapcompressedrtfstream.md) para criar uma versão descompactada dos dados RTF compactados, se disponível. 
    
5. Exibe os dados RTF não compactados ou os dados de texto sem texto para o usuário.
    
 **RTFSync** retorna um valor Boolean que indica se a mensagem foi atualizada ou não. Se esse valor retornar TRUE, chame **SaveChanges** em algum momento para tornar a atualização permanente. A chamada não precisa ser feita imediatamente após **o RTFSync** retornar. 
  
> [!NOTE]
> Como muitos componentes lidam com o texto formatado antes de você recebê-lo, há a possibilidade de corrupção. Essa corrupção pode vir do provedor do armazenamento de mensagens, de um aplicativo de terceiros, de um gateway ou de um erro de transmissão. 
  

