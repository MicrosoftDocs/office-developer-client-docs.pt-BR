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
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="f6ed2-103">Localizando enviadas ou salvo mensagens</span><span class="sxs-lookup"><span data-stu-id="f6ed2-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="f6ed2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6ed2-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f6ed2-105">**Para localizar todas as mensagens de saída que você salva ou enviado**</span><span class="sxs-lookup"><span data-stu-id="f6ed2-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="f6ed2-106">Chame [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar a pasta que contém suas mensagens enviadas com a pasta que contém suas mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6ed2-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="f6ed2-107">Defina o parâmetro _lpEntryID1_ para apontar para **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) e o parâmetro _lpEntryID2_ para apontar para **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f6ed2-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="f6ed2-108">Lembre-se de que se você excluir mensagens depois que eles são enviados ou tem movido qualquer uma das mensagens enviadas para outra pasta, essa estratégia não funcionará.</span><span class="sxs-lookup"><span data-stu-id="f6ed2-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="f6ed2-109">Se uma mensagem de entrada ao examinar notar que as propriedades que são normalmente definidas por um provedor de transporte estão ausentes, você pode assumir que a mensagem nunca foi tratada por um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f6ed2-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="f6ed2-110">Essas propriedades incluem:</span><span class="sxs-lookup"><span data-stu-id="f6ed2-110">These properties include:</span></span>
  
- <span data-ttu-id="f6ed2-111">Propriedades **PR_RECEIVED_BY**</span><span class="sxs-lookup"><span data-stu-id="f6ed2-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="f6ed2-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6ed2-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="f6ed2-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6ed2-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="f6ed2-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6ed2-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="f6ed2-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6ed2-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="f6ed2-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6ed2-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

