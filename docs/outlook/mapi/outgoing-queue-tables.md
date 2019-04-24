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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348500"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="23222-103">Tabelas de fila de saída</span><span class="sxs-lookup"><span data-stu-id="23222-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="23222-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23222-105">Uma tabela de fila de saída contém informações sobre todas as mensagens de saída de um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="23222-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="23222-106">Os provedores de repositório de mensagens implementam tabelas de fila de saída para o spooler MAPI a ser usado.</span><span class="sxs-lookup"><span data-stu-id="23222-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="23222-107">Os repositórios que não dão suporte ao envio ou recebimento de mensagens não precisam implementar essa tabela.</span><span class="sxs-lookup"><span data-stu-id="23222-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="23222-108">Para acessar uma tabela de fila de saída, o spooler MAPI chama o método [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="23222-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="23222-109">Há um requisito de que as mensagens sejam preprocessadas e enviadas ao provedor de transporte na mesma ordem em que foram enviadas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="23222-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="23222-110">O MAPI spooler é projetado para aceitar mensagens do repositório de mensagens em ordem crescente de tempo de envio.</span><span class="sxs-lookup"><span data-stu-id="23222-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="23222-111">Devido a esse requisito, pode haver um atraso antes de algumas mensagens aparecerem na tabela de fila de saída.</span><span class="sxs-lookup"><span data-stu-id="23222-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="23222-112">Os repositórios de mensagens devem permitir a classificação na tabela de fila de saída para que o spooler MAPI possa classificar as mensagens por hora de envio ou a ordem de classificação padrão deve ser em tempo de envio em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="23222-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="23222-113">A tabela de fila de saída deve enviar notificações quando o conteúdo da fila é alterado.</span><span class="sxs-lookup"><span data-stu-id="23222-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="23222-114">As propriedades a seguir compõem o conjunto de colunas necessárias nas tabelas de fila de saída:</span><span class="sxs-lookup"><span data-stu-id="23222-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23222-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23222-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="23222-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23222-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="23222-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23222-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="23222-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23222-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="23222-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="23222-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="23222-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23222-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="23222-126">Para obter mais informações sobre como a tabela de fila de saída é usada, consulte [enviando mensagens usando provedores de repositório de mensagens](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="23222-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23222-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="23222-127">See also</span></span>



[<span data-ttu-id="23222-128">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="23222-128">MAPI Tables</span></span>](mapi-tables.md)

