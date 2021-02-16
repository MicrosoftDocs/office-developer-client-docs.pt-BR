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
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="ecc32-103">Localizar Mensagens Enviadas ou Salvas</span><span class="sxs-lookup"><span data-stu-id="ecc32-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="ecc32-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecc32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ecc32-105">**Para localizar todas as mensagens de saída que você salvou ou enviou**</span><span class="sxs-lookup"><span data-stu-id="ecc32-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="ecc32-106">Chame [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) para comparar a pasta que contém suas mensagens enviadas com a pasta que contém suas mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecc32-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="ecc32-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecc32-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="ecc32-108">Esteja ciente de que, se você excluir mensagens depois que elas são enviadas ou tiver movido qualquer uma das mensagens enviadas para outra pasta, essa estratégia não funcionará.</span><span class="sxs-lookup"><span data-stu-id="ecc32-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="ecc32-109">Se ao examinar uma mensagem de entrada, você perceber que as propriedades que são normalmente definidas por um provedor de transporte estão ausentes, você pode supor que a mensagem nunca foi manipulada por um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ecc32-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="ecc32-110">Essas propriedades incluem:</span><span class="sxs-lookup"><span data-stu-id="ecc32-110">These properties include:</span></span>
  
- <span data-ttu-id="ecc32-111">**PR_RECEIVED_BY** propriedades</span><span class="sxs-lookup"><span data-stu-id="ecc32-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="ecc32-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecc32-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="ecc32-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecc32-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="ecc32-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecc32-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="ecc32-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecc32-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="ecc32-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecc32-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

