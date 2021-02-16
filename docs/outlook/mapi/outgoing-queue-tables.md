---
title: Tabelas de fila de saída
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437571"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="95ac4-103">Tabelas de fila de saída</span><span class="sxs-lookup"><span data-stu-id="95ac4-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="95ac4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95ac4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95ac4-105">Uma tabela de filas de saída contém informações sobre todas as mensagens de saída para um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="95ac4-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="95ac4-106">Os provedores de armazenamento de mensagens implementam tabelas de fila de saída para o spooler MAPI usar.</span><span class="sxs-lookup"><span data-stu-id="95ac4-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="95ac4-107">Os armazenamentos que não suportam o envio ou o recebimento de mensagens não precisam implementar esta tabela.</span><span class="sxs-lookup"><span data-stu-id="95ac4-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="95ac4-108">Para acessar uma tabela de fila de saída, o spooler MAPI chama o método [IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md)</span><span class="sxs-lookup"><span data-stu-id="95ac4-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="95ac4-109">Há um requisito para que as mensagens sejam pré-processadas e enviadas ao provedor de transporte na mesma ordem em que foram enviadas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="95ac4-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="95ac4-110">O spooler MAPI foi projetado para aceitar mensagens do armazenamento de mensagens em ordem crescente de tempo de envio.</span><span class="sxs-lookup"><span data-stu-id="95ac4-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="95ac4-111">Devido a esse requisito, pode haver algum atraso antes que algumas mensagens apareçam na tabela de filas de saída.</span><span class="sxs-lookup"><span data-stu-id="95ac4-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="95ac4-112">Os armazenamentos de mensagens devem permitir a classificação na tabela de filas de saída para que o spooler MAPI possa classificar as mensagens por hora de envio ou a ordem de classificação padrão deve ser crescente no tempo de envio.</span><span class="sxs-lookup"><span data-stu-id="95ac4-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="95ac4-113">A tabela de filas de saída deve enviar notificações quando o conteúdo da fila mudar.</span><span class="sxs-lookup"><span data-stu-id="95ac4-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="95ac4-114">As propriedades a seguir compom o conjunto de colunas necessário nas tabelas de fila de saída:</span><span class="sxs-lookup"><span data-stu-id="95ac4-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95ac4-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95ac4-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95ac4-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95ac4-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95ac4-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95ac4-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95ac4-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95ac4-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95ac4-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95ac4-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95ac4-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95ac4-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="95ac4-126">Para obter mais informações sobre como a tabela de filas de saída é usada, consulte [Enviando Mensagens Usando Provedores de Armazenamento de Mensagens.](sending-messages-by-using-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="95ac4-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95ac4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="95ac4-127">See also</span></span>



[<span data-ttu-id="95ac4-128">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="95ac4-128">MAPI Tables</span></span>](mapi-tables.md)

