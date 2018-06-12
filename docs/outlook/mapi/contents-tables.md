---
title: Tabelas de conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0dd79d9630837b5ec8a709d386ccc0db987dfb5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766304"
---
# <a name="contents-tables"></a>Tabelas de conteúdo

  
  
**Aplica-se a**: Outlook 
  
Uma tabela de conteúdo contém informações sobre objetos em um recipiente MAPI. Provedores de catálogo de endereços implementam tabelas de conteúdo para cada um dos seus contêineres e armazenamento de mensagens e provedores de transporte remoto implementam tabelas de conteúdo para suas pastas. O índice de conteúdo de um contêiner de catálogo de endereços lista informações sobre seus objetos de lista usuários e distribuição mensagens, enquanto o índice de conteúdo de uma pasta lista informações sobre suas mensagens. Tabelas de conteúdo são usadas principalmente por aplicativos do cliente. 
  
Existem dois tipos de tabelas de conteúdo de pasta:
  
- Tabelas de conteúdo padrão contêm mensagens padrão — mensagens que podem ser transmitidas e feitas visível a um usuário. 
    
- Tabelas de conteúdo associado contêm informações ocultas não transmittable criadas por um cliente para uma finalidade específica, como para armazenar uma representação alternativa de uma mensagem padrão. Informações associadas são criadas, passando o sinalizador MAPI_ASSOCIATED à chamada [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
O conteúdo que não oferecem suporte a tabelas da maioria dos contêineres de catálogo de endereços e muitas pastas categorizados classificação. 
  
Uma tabela de conteúdo pode ser acessada chamando:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) ou **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (somente pastas) especificado como a marca de propriedade e IID _IMAPITable como o identificador de interface.
    
Armazenamento de mensagens e o endereço de provedores de catálogo devem suportar ambas as técnicas para recuperar as propriedades de tabela. Ele é inaceitável para provedores dar suporte a apenas uma maneira para acessar nestas tabelas porque os clientes prevê que terá a opção. 
  
 **GetContentsTable** aceita como entrada vários sinalizadores que especificam as preferências. Quando definido, o sinalizador MAPI_ASSOCIATED recupera uma tabela de conteúdo associado. Como algumas pastas não dão suporte a conteúdo associado, e há um meio para clientes determinar isso antes do tempo, **GetContentsTable** às vezes retorna o erro MAPI_E_NO_SUPPORT quando for solicitada a uma tabela de conteúdo associado. 
  
O sinalizador MAPI_DEFERRED_ERRORS indica o implementador da tabela que quaisquer erros encontrados durante a chamada não precisam ser relatado por algum tempo. 
  
A chamada para **IMAPIProp::OpenProperty** envolve acessando uma tabela de conteúdo abrindo sua propriedade correspondente, **PR_CONTAINER_CONTENTS** para tabelas de conteúdo de catálogo de endereços e tabelas de conteúdo de pasta padrão e **PR_FOLDER_ASSOCIATED_ CONTEÚDO** para associados tabelas de conteúdo. Embora nenhuma ou essas propriedades podem ser recuperadas por meio de uma pasta ou o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner, estão incluídos na matriz de marca de propriedade que é retornado pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** também pode ser usado para incluir ou excluir uma tabela de conteúdo de uma operação de cópia. Se um cliente especifica **PR_CONTAINER_CONTENTS** no parâmetro *lpExcludeProps* para **IMAPIProp::CopyTo** em uma operação de cópia, a nova pasta ou o contêiner não dará suporte a tabela de conteúdo da pasta original ou do contêiner. 
  
Endereço livro contêiner e pasta conteúdo tabelas têm uma longa lista de colunas obrigatórias — colunas que clientes podem esperar esteja disponível depois que eles recuperam a tabela de **GetContentsTable** ou **OpenProperty**. Provedores podem adicionar a esse conjunto necessário, se necessário e clientes, por meio do método **SetColumns** , também podem solicitar modificações. 
  
As colunas obrigatórias para cada um dos tipos de tabelas de conteúdo são:
  
|**Coluna necessária**|**Tipo de tabela de conteúdo**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tabelas de pasta de transporte remoto  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Todas as tabelas de conteúdo  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Tabelas de pasta do repositório de mensagem e o contêiner de catálogo de endereços  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tabelas de pasta de transporte remoto  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
   
O identificador de entrada disponível com cada linha pode ser um curto ou longo prazo entrada identificador, dependendo da implementação da tabela. Identificadores de entrada de curto prazo geralmente são usados em situações onde é um problema de desempenho. Qualquer tipo de identificador de entrada pode ser usado para acessar o objeto correspondente. 
  
Tabelas de conteúdo também tem um conjunto de colunas que são opcionais, mas normalmente incluído por provedores de serviços em suas implementações. Essas colunas opcionais são:
  
|**Coluna opcional**|**Tipo de tabela de conteúdo**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tabelas de conteúdo de pasta padrão  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tabelas de conteúdo de pasta padrão  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tabelas de pasta de repositório de mensagens  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Todas as tabelas de conteúdo de pasta  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tabelas de contêiner de catálogo de endereços  <br/> |
   
Provedores de armazenamento de mensagem também deverá incluir **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) para tabelas de conteúdo de pastas de resultado de pesquisa somente.
  
Propriedades nomeadas podem ser adicionadas ao conjunto de coluna de uma tabela de conteúdo de pasta somente se tiverem o mesmo mapeamento assinatura, ou seja, o mesmo mapeamento de nomes de propriedade aos identificadores de propriedade de todas as mensagens na pasta. Tabelas de conteúdo de pasta devem oferecer suporte a adição de classe de mensagem propriedades específicas à coluna definidas, se eles oferecem suporte à criação de mensagens arbitrárias na pasta.
  
Clientes podem salvar a ordem de classificação padrão para uma tabela de conteúdo de pasta chamando o método [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) . Se o sinalizador RECURSIVE_SORT for especificado na chamada, a ordem de classificação pode ser feita para aplicar a todas as subpastas dentro da pasta. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

