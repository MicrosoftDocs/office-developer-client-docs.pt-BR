---
title: Suporte a texto formatado em mensagens de entrada responsabilidades do cliente
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
  
À medida que as mensagens são transferidas entre sistemas de mensagens, o spooler MAPI garante que a formatação rich text permaneça sincronizada com o texto da mensagem. O spooler MAPI chama a função [RTFSync](rtfsync.md) de dentro de uma versão empacotada da mensagem que passa para o provedor de transporte. O provedor de transporte salva as alterações feitas na mensagem chamando o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) e, em seguida, encaminha-o para o novo destinatário. 
  
Quando o aplicativo cliente de reconhecimento de RTF do destinatário abre a mensagem para exibir o texto, ele deve sincronizar o texto com a formatação e abrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , dependendo da propriedade que está disponível.
  
 **Para abrir uma mensagem, clientes com reconhecimento de RTF**
  
1. Chame **RTFSync** para sincronizar o texto da mensagem com a formatação se o repositório de mensagens não reconhece o RTF. O sinalizador RTF_SYNC_BODY_CHANGED deve ser passado no parâmetro _parâmetroulflags_ se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver ausente ou definida como false. Os clientes que trabalham com armazenamento de mensagens com reconhecimento de RTF não precisam fazer a chamada **RTFSync** porque o repositório de mensagens cuida dela. 
    
2. Chamar [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) se o texto da mensagem tiver sido atualizado. 
    
3. Chame [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** . Se **PR_RTF_COMPRESSED** não estiver disponível, você deve abrir a propriedade **PR_BODY** em vez de exibir o conteúdo da mensagem. 
    
4. Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para criar uma versão descompactado dos dados RTF compactados, se disponível. 
    
5. Exibe os dados RTF não compactados ou os dados de texto sem formatação para o usuário.
    
 **RTFSync** retorna um valor Boolean que indica se a mensagem foi atualizada ou não. Se esse valor retornar TRUE, chame **SaveChanges** em algum momento para tornar a atualização permanente. A chamada não precisa ser feita imediatamente após o **RTFSync** retornar. 
  
> [!NOTE]
> Como muitos componentes lidam com o texto formatado antes de ser recebido, há a possibilidade de corrupção. Essa corrupção pode ser proveniente do provedor de armazenamento de mensagens, de um aplicativo de terceiros, de um gateway ou de um erro de transmissão. 
  

