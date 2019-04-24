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
  
Um visualizador remoto é uma janela em um aplicativo cliente que fornece acesso controlado a mensagens armazenadas em outro computador. Esse acesso controlado pode funcionar em um link de comunicação lento. Em vez de recuperar uma seleção completa de mensagens disponíveis toda vez que um usuário abre uma pasta, o visualizador remoto exibe primeiro apenas os cabeçalhos. O usuário, em seguida, seleciona a partir dos cabeçalhos que as mensagens exibir no completo. Os clientes de visualizadores remotos podem permitir que os usuários excluam mensagens antes de serem baixadas. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Para recuperar os cabeçalhos de mensagens armazenadas remotamente
  
1. Chame [IMAPISession::](imapisession-getstatustable.md) getstatustable para acessar a tabela status. 
    
2. Call [IMAPITable:: Restrict](imapitable-restrict.md) para limitar a tabela de status apenas às linhas que têm sua coluna **tipo de recurso\_\_Pr** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) definida como provedor de transporte\_\_MAPI. 
    
3. Call [IMAPITable::](imapitable-setcolumns.md) SetColumns para incluir as seguintes colunas na tabela status: 
   - **PR\_EntryID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Métodos\_de\_recurso PR** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **Tipo\_de\_recurso PR**, **exibição\_do provedor PR\_** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR\_código\_de status** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas na tabela status. 
    
5. Passe o identificador de entrada para cada linha na tabela em uma chamada para [IMAPISession:: OpenEntry](imapisession-openentry.md). Como essa interface é empacotada do contexto de processo do spooler MAPI para o contexto de processo do cliente, diferentemente das interfaces normalmente obtidas do catálogo de endereços ou de provedores de repositório de mensagens, problemas relacionados a multithreading são mais importantes. 
    
6. Chame o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) do objeto status, passando IID_IMAPIFolder como o identificador de interface, para recuperar a pasta remota. A pasta remota não é uma implementação completa da pasta; Ele oferece suporte somente a um subconjunto de métodos e propriedades de pasta. Um dos métodos necessários, [IMAPIProp::](imapiprop-getprops.md)GetProps, oferece suporte à recuperação das seguintes propriedades:
    
    |||
    |:-----|:-----|
    |**PR\_Access** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR\_** subpastas ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    As pastas remotas também devem oferecer suporte aos métodos [IMAPIProp::](imapiprop-getproplist.md)getproplist, [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontenttable e [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) . As tabelas de conteúdo da pasta remota normalmente dão suporte às seguintes colunas: 
        
    |||
    |:-----|:-----|
    |**PR\_exibir\_para** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR\_EntryID** <br/> |
    |**PR\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Chame o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) do provedor de transporte pela primeira vez que uma das opções de transferência é separada. O sinalizador de processo REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE deve ser definido, bem como o sinalizador SHOW_XP_SSESSION_UI, para permitir a exibição da interface do usuário. 
    
   > [!NOTE]
   > Para marcar um determinado cabeçalho de mensagem para download ou exclusão, um cliente chama [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) e define o sinalizador MSGSTATUS_REMOTE_DOWNLOAD ou MSGSTATUS_REMOTE_DELETE. 
  

