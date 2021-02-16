---
title: Localizar Mensagens Enviadas ou Salvas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437417"
---
# <a name="finding-sent-or-saved-messages"></a>Localizar Mensagens Enviadas ou Salvas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para localizar todas as mensagens de saída que você salvou ou enviou**
  
1. Chame [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar a pasta que contém suas mensagens enviadas com a pasta que contém suas mensagens de entrada. 
    
2. Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
Esteja ciente de que, se você excluir mensagens depois que elas são enviadas ou tiver movido qualquer uma das mensagens enviadas para outra pasta, essa estratégia não funcionará. 
  
Se ao examinar uma mensagem de entrada, você perceber que as propriedades que são normalmente definidas por um provedor de transporte estão ausentes, você pode supor que a mensagem nunca foi manipulada por um provedor de transporte. Essas propriedades incluem:
  
- **PR_RECEIVED_BY** propriedades 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

