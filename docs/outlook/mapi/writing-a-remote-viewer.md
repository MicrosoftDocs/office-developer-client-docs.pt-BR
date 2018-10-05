---
title: Como escrever um visualizador remoto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391602"
---
# <a name="writing-a-remote-viewer"></a>Como escrever um visualizador remoto

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador remoto é uma janela em um aplicativo cliente que fornece acesso controlado às mensagens armazenadas em outro computador. Este acesso controlado pode funcionar em um link de comunicações lento. Em vez de recuperar uma seleção completa de mensagens disponíveis sempre que um usuário abre uma pasta, o visualizador remoto primeiro exibe somente os cabeçalhos. O usuário seleciona os cabeçalhos de qual das mensagens para exibir no total. Os clientes remotos visualizador podem permitir que seus usuários a excluir mensagens antes de serem baixados nunca. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Para recuperar os cabeçalhos de mensagens armazenadas remotamente
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Chamar [IMAPITable:: Restrict](imapitable-restrict.md) para limitar a tabela de status para as linhas que possuem suas **PR\_recurso\_tipo** coluna ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como MAPI\_transporte\_provedor. 
    
3. Chame [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir as seguintes colunas na tabela de status: 
   - **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR\_recurso\_métodos** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR\_recurso\_tipo**, **PR\_provedor\_exibição** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR\_STATUS\_código** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas da tabela de status. 
    
5. Passe o identificador de entrada para cada linha na tabela em uma chamada para [IMAPISession::OpenEntry](imapisession-openentry.md). Porque esta interface é enfileirada do contexto de processo do spooler MAPI para o contexto de processo do cliente — ao contrário de interfaces normalmente obtidos do catálogo de endereços ou mensagem provedores de armazenamento — problemas sobre multithreading são mais importância. 
    
6. Chame o status método do objeto [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) , passando IID_IMAPIFolder como o identificador de interface, para recuperar a pasta remota. A pasta remota não é uma implementação de pasta completa; suporte a apenas um subconjunto das propriedades e métodos de pasta. Um dos métodos necessários, [IMAPIProp::GetProps](imapiprop-getprops.md), suporta a recuperação das seguintes propriedades:
    
    |||
    |:-----|:-----|
    |**PR\_acesso** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR\_SUBPASTAS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Pastas remotas também devem suportar os métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)e [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) . Tabelas de conteúdo de pasta remota geralmente suportam as seguintes colunas: 
        
    |||
    |:-----|:-----|
    |**PR\_exibição\_para** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR\_ENTRYID** <br/> |
    |**PR\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Método a primeira hora do provedor de transporte [IMAPIStatus::ValidateState](imapistatus-validatestate.md) que uma das opções de transferência é separada da chamada. Sinalizador de processo do REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE deve ser definido, bem como o sinalizador SHOW_XP_SSESSION_UI para permitir que a interface do usuário a ser mostrado. 
    
   > [!NOTE]
   > Para marcar um cabeçalho de mensagem específica para download ou exclusão, um cliente chama [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) e define o MSGSTATUS_REMOTE_DOWNLOAD ou MSGSTATUS_REMOTE_DELETE sinalizador. 
  

