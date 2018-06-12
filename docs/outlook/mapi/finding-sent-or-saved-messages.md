---
title: Localizando enviadas ou salvo mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766564"
---
# <a name="finding-sent-or-saved-messages"></a>Localizando enviadas ou salvo mensagens

  
  
**Aplica-se a**: Outlook 
  
 **Para localizar todas as mensagens de saída que você salva ou enviado**
  
1. Chame [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar a pasta que contém suas mensagens enviadas com a pasta que contém suas mensagens de entrada. 
    
2. Defina o parâmetro _lpEntryID1_ para apontar para **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) e o parâmetro _lpEntryID2_ para apontar para **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
Lembre-se de que se você excluir mensagens depois que eles são enviados ou tem movido qualquer uma das mensagens enviadas para outra pasta, essa estratégia não funcionará. 
  
Se uma mensagem de entrada ao examinar notar que as propriedades que são normalmente definidas por um provedor de transporte estão ausentes, você pode assumir que a mensagem nunca foi tratada por um provedor de transporte. Essas propriedades incluem:
  
- Propriedades **PR_RECEIVED_BY** 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

