---
title: Enviar uma resposta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4d8c995f5fbca322fca44cdcbb0de224af6b2fbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590285"
---
# <a name="sending-a-reply"></a>Enviar uma resposta

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos de cliente geralmente oferecem suporte a dois tipos de respostas: um que será enviada somente para o remetente da mensagem original e outro que será enviada para todos os outros destinatários incluídos na lista de destinatários da mensagem original além do remetente. Este segundo tipo de resposta é comumente conhecido como uma resposta de que todas as mensagem.
  
Para enviar uma resposta de qualquer tipo, você implementar algumas das mesmas tarefas que você faria quando você envia uma mensagem original. Por exemplo, você pode abre o armazenamento de mensagens padrão e a pasta mensagens de saída, normalmente a caixa de saída e chama o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de saída da pasta para criar a resposta. Além disso, você pode abrir a pasta que contém a mensagem original, normalmente a caixa de entrada. Para obter informações sobre como abrir pastas diferentes, consulte [abrindo uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
  
A principal diferença entre uma resposta de criação e a criação de uma mensagem original é que com uma resposta, a maioria das propriedades sejam com base em ou copiada diretamente a partir de propriedades da mensagem original. Anexos — propriedade de **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) da mensagem — são especificamente excluídas. A lista de destinatários para uma resposta de todas as mensagens é criado a partir lista da mensagem original com o destinatário representado pela propriedade **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) e todos os destinatários de cópia oculta removidos. A propriedade **PR_RECEIVED_BY_SEARCH_KEY** representa o usuário atual. 
  
### <a name="to-send-a-reply"></a>Para enviar uma resposta
  
1. Abra o armazenamento de mensagens padrão. Para obter mais informações, consulte [abrindo o armazenamento de mensagens padrão](opening-the-default-message-store.md).
    
2. Abra a pasta caixa de saída. Para obter mais informações, consulte [Abrir uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
    
3. Chame o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) da caixa de saída para criar a resposta. 
    
4. Chame o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da mensagem original para copiar as seguintes propriedades para a mensagem de resposta: 
    
   - **PR\_corpo** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependendo se ou não suporte a Rich Text Format.
    
   - **PR\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), se a resposta serão encaminhadas para a lista de destinatários inteira.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Não incluem as seguintes propriedades na chamada a **IMAPIProp::CopyTo**:
    
    |||
    |:-----|:-----|
    |**PR\_cliente\_enviar\_tempo** <br/> |**PR\_mensagem\_entrega\_tempo** <br/> |
    |**PR\_mensagem\_baixar\_tempo** <br/> |**PR\_mensagem\_sinalizadores** <br/> |
    |**PR\_ORIGINADOR\_entrega\_ REPORT\REQUESTED** <br/> |**PR\_Recebidos\_REPRESENTANDO** propriedades  <br/> |
    |**PR\_ler\_recebimento\_ENTRYID** <br/> |**PR\_ler\_recebimento\_solicitado** <br/> |
    |**PR\_RECEIVED\_BY** propriedades  <br/> |**PR\_resposta\_destinatário** propriedades  <br/> |
    |**PR\_relatório\_ENTRYID** <br/> |**PR\_remetente** propriedades  <br/> |
    |**PR\_SENT\_REPRESENTANDO** propriedades  <br/> |**PR\_SENTMAIL\_ENTRYID** <br/> |
    |**PR\_assunto\_PREFIX** <br/> | <br/> |
   
6. Adicionar texto do separador a que julgar propriedade corpo da mensagem suportado — **PR_BODY**, L **PR_HTM**ou **PR_RTF_COMPRESSED**.
    
7. Chame [ScCreateConversationIndex](sccreateconversationindex.md), passando o valor da propriedade de **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) da mensagem original.
    
8. Defina um prefixo para a resposta. Se você estiver usando o padrão "RE:", concatenar esses caracteres até o início do **PR_NORMALIZED_SUBJECT** e defina **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) para essa nova cadeia de caracteres. Não defina **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Se você estiver usando um prefixo fora do padrão, como uma cadeia de caracteres com mais de três caracteres, armazene-a em **PR_SUBJECT_PREFIX**. 
    
9. Defina as propriedades **PR_SENT_REPRESENTING** com os valores correspondentes nas propriedades do **PR_RCVD_REPRESENTING** . 
    
10. Definir cada uma das entradas no **PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e **PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) com o nome de exibição e de identificador de entrada de um destinatário principal — um destinatário cujo tipo é MAPI_TO. Mantenha essas propriedades sincronizadas. Ou seja, **PR_REPLY_RECIPIENT\_ENTRADAS** **PR_REPLY_RECIPIENT_NAMES** deve conter o mesmo número de entradas e uma entrada em uma posição específica em uma das propriedades deve corresponder a uma entrada na mesma posição na outra propriedade. 
    
11. Se a resposta está sendo enviada apenas ao remetente da mensagem original, crie uma lista de destinatários de entrada única com o destinatário representado pela propriedade **PR_SENT_REPRESENTING** da mensagem original. Para obter mais informações sobre como criar uma lista de destinatários, consulte [criar uma lista do destinatário](creating-a-recipient-list.md).
    
12. Se a resposta é uma resposta a todos, crie uma lista de destinatários, da seguinte maneira:
    
    1. Chame o método de [IMessage::GetRecipientTable](imessage-getrecipienttable.md) da mensagem original para acessar sua tabela de destinatário. 
        
    2. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela. Determine se cada linha representa um destinatário primária ou cópia carbono e deve permanecer na lista ou, se ele representa um destinatário de cópia oculta ou o usuário e deve ser removido da lista. 
        
    3. Diferencie entre tipos de destinatário examinando a coluna **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta coluna será definida para MAPI_TO para destinatários principais, MAPI_CC para destinatários de cópia carbono e MAPI_BCC para os destinatários de cópia oculta. 
        
    4. Compare a coluna **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) com a propriedade **PR_RECEIVED_BY_SEARCH_KEY** da mensagem original para determinar se a linha representa o usuário. 
        
    5. Remova linhas indesejadas da lista de destinatários chamando [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória associada as entradas correspondentes na estrutura do destinatário da tabela [SRowSet](srowset.md) . Defina todos os valores da matriz de valores de propriedade como zero, todos os membros **cValues** como zero e todos os membros de **lpProps** em cada estrutura de [SRow](srow.md) no **SRowSet** como NULL. 
        
    6. Adicionar Remetente à lista de destinatários, conforme representado pela mensagem original **PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) e **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) Propriedades. Verifique se o remetente não é duplicado na lista.
        
    7. Chame o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) da mensagem reply, definindo o parâmetro _ulFlags_ como zero, para criar uma nova lista de destinatários para a resposta ou encaminhadas a mensagem com base na lista a partir da mensagem original. 
    
13. Chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) método a resposta para salvar a mensagem ou [IMessage::SubmitMessage](imessage-submitmessage.md) para salvar e enviá-la. 
    
> [!NOTE]
> Antes de chamar **IMessage::ModifyRecipients** para armazenar as alterações na lista de destinatários, você pode permitir que os usuários façam modificações por meio do formulário de mensagem. Os usuários podem adicionar à lista ou remover membros específicos. Permitindo que os usuários façam alterações em uma lista de destinatários é um recurso de cliente opcional. 
  

