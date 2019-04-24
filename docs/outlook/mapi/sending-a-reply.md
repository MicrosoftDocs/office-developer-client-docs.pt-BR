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
ms.openlocfilehash: f47741369b1091c0dd24358e063de8f4675000fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339778"
---
# <a name="sending-a-reply"></a>Enviar uma resposta

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos clientes normalmente dão suporte a dois tipos de respostas: um que é enviado somente para o remetente da mensagem original e um que é enviado a todos os outros destinatários incluídos na lista de destinatários da mensagem original, além do remetente. Esse segundo tipo de resposta costuma ser conhecido como uma mensagem de resposta a todos.
  
Para enviar uma resposta de qualquer tipo, implemente algumas das mesmas tarefas que você usaria ao enviar uma mensagem original. Por exemplo, você abre o repositório de mensagens padrão e a pasta de mensagens de saída, normalmente a saída e chama o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) da pasta de saída para criar a resposta. Além disso, abra a pasta que contém a mensagem original, normalmente a caixa de entrada. Para obter informações sobre como abrir pastas diferentes, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md).
  
A principal diferença entre a criação de uma resposta e a criação de uma mensagem original é que com uma resposta, a maioria das propriedades é baseada ou copiada diretamente das propriedades da mensagem original. Anexos – a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) de uma mensagem — são especificamente excluídas. A lista de destinatários de uma mensagem de resposta a todos é criada a partir da lista da mensagem original com o destinatário representado pela propriedade **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) e todos os destinatários de cópia carbono oculta foram removidos. A propriedade **PR_RECEIVED_BY_SEARCH_KEY** representa o usuário atual. 
  
### <a name="to-send-a-reply"></a>Para enviar uma resposta
  
1. Abra o repositório de mensagens padrão. Para obter mais informações, consulte [abrindo o repositório de mensagens padrão](opening-the-default-message-store.md).
    
2. Abra a pasta de saída. Para obter mais informações, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md).
    
3. Chame o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) da webquery para criar a resposta. 
    
4. Chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da mensagem original para copiar as seguintes propriedades para a mensagem de resposta: 
    
   - **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependendo se o formato Rich Text deve ou não ser suportado.
    
   - **PR\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), se a resposta for para toda a lista de destinatários.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Não inclua as seguintes propriedades em sua chamada para **IMAPIProp:: CopyTo**:
    
    |||
    |:-----|:-----|
    |**PR\_tempo\_de\_envio do cliente** <br/> |**PR\_tempo\_de\_entrega de mensagem** <br/> |
    |**Tempo\_de\_download\_de mensagem PR** <br/> |**Sinalizadores\_de\_mensagem PR** <br/> |
    |**PR\_REPORT\REQUESTED\_de\_ entrega de originador** <br/> |**PR\_recebidos\_representando** Propriedades  <br/> |
    |**PR\_EntryID\_de confirmação de leitura\_** <br/> |**PR\_confirmação\_\_de leitura solicitada** <br/> |
    |**PR\_recebidas\_por** Propriedades  <br/> |Propriedades do **destinatário da resposta PR\_\_**  <br/> |
    |**PR\_de\_relatório de entrada** <br/> |**PR\_** Propriedades do remetente  <br/> |
    |**PR\_propriedades\_de representação** remetidas  <br/> |**PR\_SENTMAIL\_EntryID** <br/> |
    |**PR\_prefixo\_de assunto** <br/> | <br/> |
   
6. Adicione texto separador a qualquer Propriedade do corpo da mensagem suportada — **PR_BODY**, **PR_HTM**L ou **PR_RTF_COMPRESSED**.
    
7. Chame [ScCreateConversationIndex](sccreateconversationindex.md), passando o valor da propriedade **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) da mensagem original.
    
8. Definir um prefixo para a resposta. Se você estiver usando o padrão "RE:", concatene esses caracteres no início do **PR_NORMALIZED_SUBJECT** e defina **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) para essa nova cadeia de caracteres. Não defina **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Se você estiver usando um prefixo não padrão, como uma cadeia de caracteres com mais de três caracteres, armazene-o no **PR_SUBJECT_PREFIX**. 
    
9. Defina as propriedades de **PR_SENT_REPRESENTING** para os valores correspondentes nas propriedades de **PR_RCVD_REPRESENTING** . 
    
10. Defina cada uma das entradas em **PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e **PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) para o identificador de entrada e o nome de exibição de um destinatário principal — um destinatário cujo tipo é MAPI_TO. Mantenha essas propriedades sincronizadas. Ou seja, **as\_entradas PR_REPLY_RECIPIENT** e **PR_REPLY_RECIPIENT_NAMES** devem conter o mesmo número de entradas, e uma entrada em uma posição específica em uma das propriedades deve corresponder a uma entrada na mesma posição no outro Propriedades. 
    
11. Se a resposta estiver sendo enviada apenas ao remetente da mensagem original, crie uma única lista de destinatários de entrada com o destinatário representado pela propriedade **PR_SENT_REPRESENTING** da mensagem original. Para obter mais informações sobre como criar uma lista de destinatários, consulte [Creating a Recipient List](creating-a-recipient-list.md).
    
12. Se a resposta for uma resposta a todos, crie uma lista de destinatários da seguinte maneira:
    
    1. Chame o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable da mensagem original para acessar sua tabela de destinatários. 
        
    2. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela. Determine se cada linha representa um destinatário principal ou de cópia carbono e deve permanecer na lista ou se ele representa um destinatário de cópia oculta ou o usuário e deve ser removido da lista. 
        
    3. Para diferenciar os tipos de destinatários, examine a coluna **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta coluna será definida como MAPI_TO para destinatários principais, MAPI_CC para destinatários de cópia carbono e MAPI_BCC para destinatários de cópia oculta. 
        
    4. Compare a coluna **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) com a propriedade **PR_RECEIVED_BY_SEARCH_KEY** da mensagem original para determinar se a linha representa o usuário. 
        
    5. Remova as linhas indesejadas da lista de destinatários chamando [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória associada às entradas correspondentes na estrutura [SRowSet](srowset.md) da tabela de destinatários. Defina todos os valores na matriz de valor da propriedade como zero, todos os membros **cValues** como zero e todos os membros **lpProps** em cada estrutura [SRow](srow.md) no **SRowSet** como nulo. 
        
    6. Adicionar o remetente à lista de destinatários, conforme representado pela **SENT_REPRESENTING_NAME de\_RP** da mensagem original ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) e **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) Propriedades. Verifique se o remetente não está duplicado na lista.
        
    7. Chame o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) da mensagem de resposta, definindo o parâmetro _parâmetroulflags_ como zero, para criar uma nova lista de destinatários para a resposta ou mensagem encaminhada com base na lista da mensagem original. 
    
13. Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da resposta para salvar a mensagem ou [IMessage:: SubmitMessage](imessage-submitmessage.md) para salvá-la e enviá-la. 
    
> [!NOTE]
> Antes de chamar **IMessage:: ModifyRecipients** para armazenar as alterações na lista de destinatários, você pode permitir que os usuários façam modificações através do formulário de mensagem. Os usuários podem adicionar à lista ou remover membros específicos. Permitir que os usuários façam alterações em uma lista de destinatários é um recurso de cliente opcional. 
  

