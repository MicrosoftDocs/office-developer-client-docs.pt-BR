---
title: Tabelas de conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335592"
---
# <a name="contents-tables"></a>Tabelas de conteúdo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de conteúdo contém informações sobre objetos em um contêiner MAPI. Os provedores de catálogo de endereços implementam tabelas de conteúdo para cada um de seus contêineres, e o repositório de mensagens e os provedores de transporte remoto implementam tabelas de conteúdo para suas pastas A tabela de conteúdo de um contêiner de catálogo de endereços lista informações sobre seus usuários de mensagens e objetos de lista de distribuição, enquanto a tabela de conteúdo de uma pasta lista informações sobre suas mensagens. As tabelas de conteúdo são usadas principalmente por aplicativos cliente. 
  
Há dois tipos de tabelas de conteúdo da pasta:
  
- Tabelas de conteúdo padrão contêm mensagens padrão — mensagens que podem ser transmitidas e tornadas visíveis para um usuário. 
    
- As tabelas de conteúdo associadas contêm informações ocultas, não transmisstable criadas por um cliente para uma finalidade específica, como armazenar uma representação alternativa de uma mensagem padrão. As informações associadas são criadas passando o sinalizador MAPI_ASSOCIATED para a chamada [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . 
    
As tabelas de conteúdo da maioria dos contêineres do catálogo de endereços e muitas pastas não oferecem suporte à classificação classificada. 
  
Uma tabela de conteúdo pode ser acessada chamando:
  
- [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontenttable.
    
    - Ou
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) com **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) ou **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (apenas pastas) especificadas como marca de propriedade e IID _IMAPITable como o identificador de interface.
    
O repositório de mensagens e os provedores de catálogo de endereços devem dar suporte a ambas as técnicas para recuperar as propriedades da tabela. É inaceitável que os provedores só ofereçam suporte a uma maneira de acessar essas tabelas porque os clientes esperam ter a opção. 
  
 **** Getcontenttable aceita como entrada vários sinalizadores que especificam preferências. Quando definido, o sinalizador MAPI_ASSOCIATED recupera uma tabela de conteúdo associada. Como algumas pastas não dão suporte a conteúdo associado e não há nenhuma forma de os clientes determinarem isso antes do tempo **** , getcontenttable às vezes retorna o erro MAPI_E_NO_SUPPORT quando uma tabela de conteúdo associado é solicitada. 
  
O sinalizador MAPI_DEFERRED_ERRORS indica ao implementador da tabela que os erros encontrados durante a chamada não precisam ser relatados até um momento posterior. 
  
A chamada para **IMAPIProp:: OpenProperty** envolve acessar uma tabela de conteúdo abrindo sua propriedade correspondente, **PR_CONTAINER_CONTENTS** para tabelas de conteúdo de catálogo de endereços e tabelas de conteúdo de pastas padrão e **PR_FOLDER_ASSOCIATED_ CONTEÚDO** das tabelas de conteúdo associado. Embora nenhuma ou essas propriedades possam ser recuperadas por meio de um método [IMAPIProp::](imapiprop-getprops.md) GetProps de pasta ou contêiner, elas estão incluídas na matriz de marca de propriedade retornada pelo método [IMAPIProp::](imapiprop-getproplist.md) getproplist. 
  
 **PR_CONTAINER_CONTENTS** também pode ser usado para incluir ou excluir uma tabela de conteúdo de uma operação de cópia. Se um cliente especificar **PR_CONTAINER_CONTENTS** no parâmetro *lpExcludeProps* para **IMAPIProp:: CopyTo** em uma operação de cópia, a nova pasta ou contêiner não terá suporte para a tabela de conteúdo da pasta ou contêiner original. 
  
O contêiner do catálogo de endereços e as tabelas de conteúdo da pasta têm uma lista extensa de colunas obrigatórias — colunas que os clientes podem esperar que estejam **** disponíveis após a recuperação da tabela de getcontenttable ou **OpenProperty**. Os provedores podem adicionar a esse conjunto obrigatório se necessário, e os clientes **** , através do método SetColumns, também podem solicitar modificações. 
  
As colunas obrigatórias para cada um dos tipos de tabelas de conteúdo são:
  
|**Coluna Required**|**Tabela de tipos de conteúdo**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tabelas de pastas de transporte remoto  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Contêiner de catálogo de endereços e tabelas de pastas de repositório de mensagens  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tabelas de pastas de transporte remoto  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
   
O identificador de entrada disponível com cada linha pode ser um identificador de entrada de curto ou longo prazo, dependendo da implementação da tabela. Identificadores de entrada de curto prazo são geralmente usados em situações em que o desempenho é um problema. Qualquer tipo de identificador de entrada pode ser usado para acessar o objeto correspondente. 
  
As tabelas de conteúdo também têm um conjunto de colunas que são opcionais, mas que normalmente são incluídos por provedores de serviços em suas implementações. Essas colunas opcionais são:
  
|**Coluna opcional**|**Tabela de tipos de conteúdo**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tabelas de conteúdo da pasta padrão  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tabelas de conteúdo da pasta padrão  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tabelas de pastas de repositório de mensagens  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Todas as tabelas de conteúdo da pasta  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
   
Os provedores de repositórios de mensagens também devem incluir **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) somente para tabelas de conteúdo de pastas de resultados de pesquisa.
  
Propriedades nomeadas podem ser adicionadas ao conjunto de colunas de uma tabela de conteúdo da pasta somente se todas as mensagens na pasta tiverem a mesma assinatura de mapeamento, ou seja, o mesmo mapeamento de nomes de propriedade para identificadores de propriedade. As tabelas de conteúdo da pasta devem oferecer suporte à adição de propriedades específicas de classe de mensagem para o conjunto de colunas, se eles oferecem suporte à criação de mensagens arbitrárias na pasta.
  
Os clientes podem salvar a ordem de classificação padrão para uma tabela de conteúdo da pasta chamando o método [IMAPIFolder:: SaveContentsSort](imapifolder-savecontentssort.md) . Se o sinalizador RECURSIVE_SORT for especificado na chamada, a ordem de classificação poderá ser feita para ser aplicada a todas as subpastas dentro da pasta. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

