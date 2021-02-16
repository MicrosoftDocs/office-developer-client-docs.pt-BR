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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437445"
---
# <a name="sending-a-reply"></a>Enviar uma resposta

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente normalmente suportam dois tipos de respostas: um enviado apenas para o remetente da mensagem original e outro para todos os outros destinatários incluídos na lista de destinatários da mensagem original, além do remetente. Esse segundo tipo de resposta é normalmente chamado de mensagem de resposta a todos.
  
Para enviar uma resposta de qualquer tipo, implemente algumas das mesmas tarefas que faria ao enviar uma mensagem original. Por exemplo, você abre o armazenamento de mensagens padrão e a pasta de mensagens de saída, normalmente a Caixa de Saída, e chama o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) da pasta de saída para criar a resposta. Além disso, você abre a pasta que contém a mensagem original, normalmente a Caixa de Entrada. Para obter informações sobre como abrir pastas diferentes, consulte [Abrir uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md)
  
A principal diferença entre criar uma resposta e criar uma mensagem original é que, com uma resposta, a maioria das propriedades é baseada ou copiada diretamente das propriedades da mensagem original. Anexos — a propriedade PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) de uma mensagem — são especificamente excluídos. A lista de destinatários de uma resposta a todas as mensagens é criada a partir da lista da mensagem original com o destinatário representado pela propriedade **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) e todos os destinatários com cópia carbono são removidos. A **PR_RECEIVED_BY_SEARCH_KEY** propriedade representa o usuário atual. 
  
### <a name="to-send-a-reply"></a>Para enviar uma resposta
  
1. Abra o armazenamento de mensagens padrão. Para obter mais informações, consulte [Abrindo o Armazenamento de Mensagens Padrão.](opening-the-default-message-store.md)
    
2. Abra a pasta Caixa de Saída. Para obter mais informações, consulte [Abrindo uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md)
    
3. Chame o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) da Caixa de Saída para criar a resposta. 
    
4. Chame o método [IMAPIProp::CopyTo](imapiprop-copyto.md) da mensagem original para copiar as seguintes propriedades para a mensagem de resposta: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependendo se você dá suporte ou não ao formato Rich Text.
    
   - **PR \_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), se a resposta for para toda a lista de destinatários.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Não inclua as seguintes propriedades em sua chamada para **IMAPIProp::CopyTo**:
    
    |||
    |:-----|:-----|
    |**HORÁRIO DE \_ ENVIO \_ DO CLIENTE \_ PR** <br/> |**HORA DE \_ ENTREGA DA MENSAGEM DE \_ \_ PR** <br/> |
    |**HORÁRIO DE \_ DOWNLOAD DA MENSAGEM DE \_ \_ PR** <br/> |**SINALIZADORES \_ \_ DE MENSAGEM DE PR** <br/> |
    |**RELATÓRIO \_ DE ENTREGA DO \_ ORIGINADOR DE \_ PR\SOLICITADO** <br/> |**PR \_ RCVD \_ REPRESENTING** properties  <br/> |
    |**ENTRYID \_ DE CONFIRMAÇÃO DE LEITURA DE \_ \_ PR** <br/> |**CONFIRMAÇÃO DE LEITURA DE PR \_ \_ \_ SOLICITADA** <br/> |
    |**PR \_ PROPRIEDADES RECEIVED \_ BY**  <br/> |**PR \_ PROPRIEDADES \_ DE DESTINATÁRIO DE** RESPOSTA  <br/> |
    |**ENTRYID \_ DO \_ RELATÓRIO DE PR** <br/> |**PR \_ Propriedades do** REMETENTE  <br/> |
    |**PR \_ SENT \_ REPRESENTING** properties  <br/> |**PR \_ SENTMAIL \_ ENTRYID** <br/> |
    |**PREFIXO \_ DE ASSUNTO \_ PR** <br/> | <br/> |
   
6. Adicione texto separador a qualquer propriedade do corpo da mensagem que você suporte — **PR_BODY,** **PR_HTM** L ou **PR_RTF_COMPRESSED**.
    
7. Chame [ScCreateConversationIndex](sccreateconversationindex.md), passando o valor da propriedade **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) da mensagem original.
    
8. Definir um prefixo para a resposta. Se você estiver usando o padrão "RE:", concatene esses caracteres no início de **PR_NORMALIZED_SUBJECT** e de definir **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) para essa nova cadeia de caracteres. Não definir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Se você estiver usando um prefixo não padrão, como uma cadeia de caracteres com mais de três caracteres, armazene-o **PR_SUBJECT_PREFIX**. 
    
9. De **definidas PR_SENT_REPRESENTING** propriedades com os valores correspondentes nas **propriedades PR_RCVD_REPRESENTING** propriedades. 
    
10. Definir cada uma das entradas em **PR \_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e **PR_REPLY \_ RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) para o identificador de entrada e o nome de exibição de um destinatário primário — um destinatário cujo tipo é MAPI_TO. Mantenha essas propriedades sincronizadas. Ou seja, **PR_REPLY_RECIPIENT \_ ENTRIES** e **PR_REPLY_RECIPIENT_NAMES** devem conter o mesmo número de entradas, e uma entrada em uma posição específica em uma das propriedades deve corresponder a uma entrada na mesma posição na outra propriedade. 
    
11. Se a resposta estiver sendo enviada apenas para o remetente da mensagem original, crie uma lista de destinatários de entrada única com o destinatário representado pela propriedade PR_SENT_REPRESENTING **mensagem** original. Para obter mais informações sobre como criar uma lista de destinatários, consulte [Criando uma lista de destinatários.](creating-a-recipient-list.md)
    
12. Se a resposta for uma resposta a todos, crie uma lista de destinatários da seguinte forma:
    
    1. Chame o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) da mensagem original para acessar sua tabela de destinatários. 
        
    2. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela. Determine se cada linha representa um destinatário de cópia primária ou carbono e deve permanecer na lista ou se ela representa um destinatário com cópia carbono ou o usuário e deve ser removida da lista. 
        
    3. Diferencie entre tipos de destinatários observando **a PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Essa coluna será definida como MAPI_TO para destinatários primários, MAPI_CC para destinatários de cópia carbono e MAPI_BCC destinatários com cópia carbono. 
        
    4. Compare a **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) com a propriedade **PR_RECEIVED_BY_SEARCH_KEY** da mensagem original para determinar se a linha representa o usuário. 
        
    5. Remova linhas indesejadas da lista de destinatários chamando [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória associada às entradas correspondentes na estrutura [SRowSet](srowset.md) da tabela de destinatários. De definir todos os valores na matriz de valores de propriedade como zero, todos os membros **cValues** como zero e todos os membros **lpProps** em cada estrutura [SRow](srow.md) no **SRowSet** como NULL. 
        
    6. Adicione o remetente à lista de destinatários, conforme representado pelas propriedades **PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) e **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) da mensagem original. Verifique se o remetente não está duplicado na lista.
        
    7. Chame o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) da mensagem de resposta, definindo o  _parâmetro ulFlags_ como zero, para criar uma nova lista de destinatários para a mensagem de resposta ou encaminhada com base na lista da mensagem original. 
    
13. Chame o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da resposta para salvar a mensagem ou [IMessage::SubmitMessage](imessage-submitmessage.md) para salvá-la e enviá-la. 
    
> [!NOTE]
> Antes de **chamar IMessage::ModifyRecipients** para armazenar alterações na lista de destinatários, você pode permitir que os usuários façam modificações por meio do formulário de mensagem. Os usuários podem adicionar à lista ou remover membros específicos. Permitir que os usuários façam alterações em uma lista de destinatários é um recurso opcional do cliente. 
  

