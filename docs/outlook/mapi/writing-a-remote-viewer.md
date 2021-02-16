---
title: Gravar um visualizador remoto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325659"
---
# <a name="writing-a-remote-viewer"></a>Gravar um visualizador remoto

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador remoto é uma janela em um aplicativo cliente que fornece acesso controlado a mensagens armazenadas em outro computador. Esse acesso controlado pode operar em um link de comunicações lentas. Em vez de recuperar uma seleção completa de mensagens disponíveis sempre que um usuário abre uma pasta, o visualizador remoto exibe primeiro apenas os títulos. Em seguida, o usuário seleciona entre os headers qual das mensagens exibir na íntegra. Os clientes do visualizador remoto podem permitir que seus usuários excluam mensagens antes que sejam baixados. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Para recuperar os headers das mensagens armazenadas remotamente
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Chame [IMAPITable::Restrict](imapitable-restrict.md) para limitar a tabela de status apenas às linhas que têm sua coluna TIPO de RECURSO PR ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como MAPI TRANSPORT **\_ \_** \_ \_ PROVIDER. 
    
3. Chame [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir as seguintes colunas na tabela de status: 
   - **PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR \_ RESOURCE \_ METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR \_ TIPO \_ DE RECURSO**, **\_ \_ EXIBIÇÃO DO PROVEDOR DE** PR ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR \_ CÓDIGO \_ DE STATUS** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela de status. 
    
5. Passe o identificador de entrada para cada linha na tabela em uma chamada para [IMAPISession::OpenEntry](imapisession-openentry.md). Como essa interface é empacotada do contexto de processo do spooler MAPI para o contexto de processo do cliente — ao contrário das interfaces normalmente obtidas do livro de endereços ou dos provedores de armazenamento de mensagens — questões referentes a multithreading são mais importantes. 
    
6. Chame o método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) do objeto de status, passando IID_IMAPIFolder como o identificador da interface, para recuperar a pasta remota. A pasta remota não é uma implementação de pasta completa; ele dá suporte apenas a um subconjunto de métodos e propriedades de pasta. Um dos métodos necessários, [IMAPIProp::GetProps](imapiprop-getprops.md), oferece suporte à recuperação das seguintes propriedades:
    
    |||
    |:-----|:-----|
    |**PR \_ ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR \_ SUBPASTAS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    As pastas remotas também devem dar suporte aos métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)e [IMAPIFolder::SetMessageStatus.](imapifolder-setmessagestatus.md) As tabelas de conteúdo de pastas remotas normalmente suportam as seguintes colunas: 
        
    |||
    |:-----|:-----|
    |**PR \_ DISPLAY \_ TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR \_ ENTRYID** <br/> |
    |**PR \_ HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR \_ MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR \_ MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Chame o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do provedor de transporte na primeira vez que uma das opções de transferência for escolhida. O sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE processo deve ser definido, bem como o sinalizador SHOW_XP_SSESSION_UI para permitir que a interface do usuário seja mostrada. 
    
   > [!NOTE]
   > Para marcar um determinado header de mensagem para download ou exclusão, um cliente chama [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) e define o sinalizador MSGSTATUS_REMOTE_DOWNLOAD ou MSGSTATUS_REMOTE_DELETE. 
  

