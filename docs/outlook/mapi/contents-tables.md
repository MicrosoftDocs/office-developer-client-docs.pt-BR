---
title: Tabelas de Conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435583"
---
# <a name="contents-tables"></a>Tabelas de Conteúdo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de conteúdo contém informações sobre objetos em um contêiner MAPI. Os provedores de agenda implementam tabelas de conteúdo para cada um de seus contêineres, e o armazenamento de mensagens e os provedores de transporte remoto implementam tabelas de conteúdo para suas pastas. O índice de conteúdo de um contêiner de livro de endereços lista informações sobre seus objetos de lista de distribuição e usuário de mensagens, enquanto o índice de uma pasta lista informações sobre suas mensagens. Tabelas de conteúdo são usadas principalmente por aplicativos cliente. 
  
Há dois tipos de tabelas de conteúdo de pastas:
  
- Tabelas de conteúdo padrão contêm mensagens padrão — mensagens que podem ser transmitidas e visíveis para um usuário. 
    
- Tabelas de conteúdo associadas contêm informações ocultas, não transmitíveis criadas por um cliente para uma finalidade específica, como para armazenar uma representação alternativa de uma mensagem padrão. As informações associadas são criadas passando o sinalizador MAPI_ASSOCIATED para a chamada [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) 
    
Os índices de conteúdo da maioria dos contêineres de agendamento de endereços e muitas pastas não suportam classificação categorizada. 
  
Uma tabela de conteúdo pode ser acessada chamando:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com PR_CONTAINER_CONTENTS ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) ou **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) especificados como **a** marca de propriedade e IID_IMAPITable como o identificador da interface.
    
Os provedores de armazenamento de mensagens e de agendamento de endereços devem dar suporte a ambas as técnicas para recuperar as propriedades da tabela. É inaceitável para os provedores dar suporte apenas a uma maneira de acessar essas tabelas, pois os clientes esperam ter a opção. 
  
 **GetContentsTable** aceita como entrada vários sinalizadores que especificam preferências. Quando definido, o MAPI_ASSOCIATED sinalizador recupera uma tabela de conteúdo associada. Como algumas pastas não suportam conteúdo associado e não há como os clientes determinarem isso com antecedência, **GetContentsTable** às vezes retorna o erro MAPI_E_NO_SUPPORT quando uma tabela de conteúdo associada é solicitada. 
  
O MAPI_DEFERRED_ERRORS sinalizador indica ao implementador da tabela que quaisquer erros encontrados durante a chamada não precisam ser relatados até algum momento posterior. 
  
A chamada para **IMAPIProp::OpenProperty** envolve acessar uma tabela de conteúdo abrindo sua propriedade correspondente, **PR_CONTAINER_CONTENTS** para tabelas de conteúdo de agendamento de endereços e tabelas de conteúdo de pasta padrão e **PR_FOLDER_ASSOCIATED_CONTENTS** tabelas de conteúdo associadas. Embora nenhuma dessas propriedades possa ser recuperada por meio de uma pasta ou do método [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner, elas são incluídas na matriz de marca de propriedade que é retornada pelo método [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_CONTENTS** também pode ser usado para incluir ou excluir um índice de conteúdo de uma operação de cópia. Se um cliente especificar PR_CONTAINER_CONTENTS no parâmetro *lpExcludeProps* para **IMAPIProp::CopyTo** em uma operação de cópia, a nova pasta ou contêiner não dará suporte **ao** índice de conteúdo da pasta ou contêiner original. 
  
As tabelas de conteúdo de pastas e contêineres de listas de endereços têm uma longa lista de colunas necessárias — colunas que os clientes podem esperar disponibilizar depois de recuperar a tabela de **GetContentsTable** ou **OpenProperty**. Os provedores podem adicionar a esse conjunto necessário, se necessário, e os clientes, por meio do **método SetColumns,** também podem solicitar modificações. 
  
As colunas necessárias para cada um dos tipos de tabelas de conteúdo são:
  
|**Coluna necessária**|**Tipo de tabela de conteúdo**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tabelas de pastas de transporte remoto  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Tabelas de pastas do contêiner e do armazenamento de mensagens do address book  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tabelas de pastas de transporte remoto  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
   
O identificador de entrada disponível com cada linha pode ser um identificador de entrada de curto ou longo prazo, dependendo da implementação da tabela. Os identificadores de entrada de curto prazo geralmente são usados em situações em que o desempenho é um problema. Qualquer tipo de identificador de entrada pode ser usado para acessar o objeto correspondente. 
  
Os índices de conteúdo também têm um conjunto de colunas que são opcionais, mas normalmente incluídas pelos provedores de serviços em suas implementações. Essas colunas opcionais são:
  
|**Coluna opcional**|**Tipo de tabela de conteúdo**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tabelas de conteúdo de pastas padrão  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tabelas de conteúdo de pastas padrão  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tabelas de pastas do armazenamento de mensagens  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pastas  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tabelas de contêiner do livro de endereços  <br/> |
   
Os provedores de armazenamento de mensagens também devem **incluir PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) somente para tabelas de conteúdo de pastas de resultados de pesquisa.
  
Propriedades nomeadas podem ser adicionadas ao conjunto de colunas de uma tabela de conteúdo de pasta somente se todas as mensagens na pasta têm a mesma assinatura de mapeamento, ou seja, o mesmo mapeamento de nomes de propriedade para identificadores de propriedade. As tabelas de conteúdo da pasta devem dar suporte à adição de propriedades específicas da classe de mensagens ao conjunto de colunas, se elas deem suporte à criação de mensagens arbitrárias na pasta.
  
Os clientes podem salvar a ordem de classificação padrão para uma tabela de conteúdo de pasta chamando seu método [IMAPIFolder::SaveContentsSort.](imapifolder-savecontentssort.md) Se o RECURSIVE_SORT sinalizador for especificado na chamada, a ordem de classificação poderá ser feita para aplicar a todas as subpastas dentro da pasta. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

