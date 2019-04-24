---
title: Mapeamento de atributos TNEF para propriedades MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 25647a6488fec9a39f8b41441fe9afc4c4aa0a7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357649"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>Mapeamento de atributos TNEF para propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela a seguir lista todos os atributos definidos na implementação do TNEF e seus mapeamentos para propriedades MAPI. Em alguns casos, várias propriedades MAPI são codificadas como um único atributo. Alguns atributos têm descrições estendidas posteriormente nesta seção.
  
|**Atributo TNEF**|**Propriedade ou propriedades MAPI**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID** ([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**attAttachment** <br/> |Para obter informações sobre esse mapeamento, consulte [atributos TNEF](tnef-attributes.md).  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**attBody** <br/> |**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY** ([PidTagConversationKey](pidtagconversationkey-canonical-property.md)) Essa propriedade foi preterida no Microsoft Exchange Server: seu uso persiste no Outlook apenas para localizar **IPM. **Mensagens de MessageManager.  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) ConFira os [atributos attDate](attdate-attributes.md) para obter detalhes.  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME** ConFira os [atributos attDate](attdate-attributes.md) para obter detalhes.  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) ConFira os [atributos attDate](attdate-attributes.md) para obter detalhes.  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) ConFira os [atributos attDate](attdate-attributes.md) para obter detalhes.  <br/> |
|**attDateStart** <br/> |**PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) ConFira os [atributos attDate](attdate-attributes.md) para obter detalhes.  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) e **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |Para obter informações sobre esse atributo, consulte [attMAPIProps](attmapiprops.md).  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**attMessageID** <br/> |**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) ConFira a [correlação de TNEF nos gatewayS X. 400 e transportes](tnef-correlation-in-x-400-gateways-and-transports.md).  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |Consulte [attOwner](attowner.md).  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY** (**PidTagParentKey**) Essa propriedade foi preterida. Consulte [API elementos preteridos nesta edição](api-elements-deprecated-in-this-edition.md) para obter mais informações.  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED** ([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**attSubject** <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

