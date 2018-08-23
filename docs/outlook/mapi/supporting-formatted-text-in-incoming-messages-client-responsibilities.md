---
title: Suporte formatado o texto no responsabilidades de cliente de mensagens recebidas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d8fdd9ea4dfbc40d7e800be5e2df666738d2cd23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577454"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como as mensagens são transferidas entre sistemas de mensagens, o MAPI spooler certifica-se de que a formatação rich text permanecerá sincronizada com o texto da mensagem. O MAPI spooler chama a função de [RTFSync](rtfsync.md) de dentro de uma versão com quebra da mensagem que ele passa para o provedor de transporte. O provedor de transporte salva as alterações feitas à mensagem chamando o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e encaminha para o novo destinatário. 
  
Quando o aplicativo de cliente RTF reconhecimento do destinatário abre a mensagem para exibir o texto, ele deve sincronizar o texto com formatação e abra **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , dependendo de qual propriedade está disponível.
  
 **Para abrir uma mensagem, os clientes de RTF**
  
1. Chame **RTFSync** para sincronizar o texto da mensagem com a formatação se o armazenamento de mensagens não é sensível ao RTF. O sinalizador RTF_SYNC_BODY_CHANGED deve ser passado no parâmetro _ulFlags_ se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver faltando ou defina como FALSE. Trabalhando com reconhecimento de RTF armazenamentos de mensagens de clientes não precisam fazer a chamada **RTFSync** porque o armazenamento de mensagens cuida disso. 
    
2. Chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) se o texto da mensagem foi atualizado. 
    
3. Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** . Se **PR_RTF_COMPRESSED** não estiver disponível, você deve abrir a propriedade **PR_BODY** em vez disso, para exibir o conteúdo da mensagem. 
    
4. Chame a função de [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para criar uma versão descompactada dos dados compactados RTF, se disponível. 
    
5. Exiba os dados RTF descompactados ou os dados de texto sem formatação para o usuário.
    
 **RTFSync** retorna um valor Boolean que indica se ou não a mensagem foi atualizada. Se esse valor retornar TRUE, chame **SaveChanges** em algum momento para fazer a atualização permanente. A chamada não tem a ser feita imediatamente após **RTFSync** retorna. 
  
> [!NOTE]
> Como componentes tantos manipular o texto formatado antes de você recebê-la, há a possibilidade dos danos. Essa corrupção poderia provenientes de um aplicativo de terceiros, o provedor de armazenamento de mensagem, um gateway ou um erro de transmissão. 
  

